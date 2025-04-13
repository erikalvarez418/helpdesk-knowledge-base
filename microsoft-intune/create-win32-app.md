# How to Create a Win32 App in Intune

## Summary
Win32 apps are used in Intune to deploy traditional Windows apps (EXE, MSI) packaged into the `.intunewin` format. This allows for advanced install logic, detection rules, and deployment flexibility.

---

## Prerequisites

- App install files (EXE, MSI, or full folder)
- Basic install command (e.g., setup.exe /silent)
- Access to the Microsoft Win32 Content Prep Tool: https://github.com/Microsoft/Microsoft-Win32-Content-Prep-Tool
- Admin access to Microsoft Endpoint Manager: https://endpoint.microsoft.com

---

## Step 1: Package the App into `.intunewin` Format

1. Download the Win32 Content Prep Tool from the GitHub link above.

2. Extract the tool to a folder (e.g., C:\IntuneWinAppUtil)

3. Run the tool:
   - Open PowerShell
   - Navigate to the folder where IntuneWinAppUtil.exe is located
   - Run: 
     .\IntuneWinAppUtil.exe

4. When prompted:
   - Source folder: Location of your installer files (e.g., C:\Installers\Zoom)
   - Setup file: Your actual install file (e.g., ZoomInstallerFull.exe)
   - Output folder: Where you want the `.intunewin` file to be saved

5. The tool will generate a file like:
   ZoomInstallerFull.intunewin

---

## Step 2: Upload App to Intune

1. Go to: https://endpoint.microsoft.com

2. Navigate to:
   Apps > Windows > Add

3. Choose App type: Windows app (Win32)

4. Upload the `.intunewin` file created earlier

---

## Step 3: Configure App Information

- Name: Clear and descriptive (e.g., Zoom Client - Win32)
- Description: Optional, shows up in Company Portal
- Publisher: e.g., Zoom Video Communications
- Category: Optional but recommended for organization

---

## Step 4: Set Program Install/Uninstall Commands

Install command example:
  ZoomInstallerFull.exe /quiet /norestart

Uninstall command example:
  msiexec /x {Zoom-GUID-HERE} /quiet

Tip: You can find uninstall strings in the registry or with tools like Revo Uninstaller.

---

## Step 5: Configure Detection Rules

Detection rules tell Intune when the app is successfully installed.

Most common method: File or folder exists  
- Path: C:\Program Files (x86)\Zoom\bin\Zoom.exe  
- Detection type: File exists

You can also use MSI product code or registry-based detection.

---

## Step 6: Set Requirements (Optional)

Examples:
- Operating system: Windows 10 1909 or later
- Architecture: 64-bit
- Minimum RAM: 8 GB (for large apps)

---

## Step 7: Assign the App

- Choose assignment type:
  - Required = Auto-install
  - Available for enrolled devices = User-initiated via Company Portal

- Assign to user or device groups

---

## Step 8: Monitor the Deployment

Go to:  
Apps > Monitor > App install status

Filter by app or device. Check status:
- Installed
- Failed
- Not applicable
- Pending

---

## Notes

- Win32 apps support more complex deployment logic than LOB apps
- Use detection rules wisely to prevent endless retry loops
- Combine with PowerShell scripts or dependencies for chained installs

---

## Related Articles

- [App Not Deploying in Intune](./app-not-deploying.md)
- [Policy Not Applying to Device](./policy-not-applying.md)
- [Re-Enroll a Device in Intune](./reenroll-device.md)
