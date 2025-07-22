# WinGetInstall
Install WinGet on PC (like Win 10 or older versions)

How to install winget on Win10 PC that doesn't recognize winget?
To install winget on a Windows 10 PC that doesn't recognize the winget command, you have several options:

Option 1: Install from Microsoft Store (Recommended)
1. Open Microsoft Store
2. Search for "App Installer" 
3. Install or update the "App Installer" app
4. Winget comes bundled with App Installer

Option 2: Download from GitHub
1. Go to the winget GitHub releases page: <a href="https://github.com/microsoft/winget-cli/releases">https://github.com/microsoft/winget-cli/releases</a>
2. Download the latest <code>.msixbundle</code> file
3. Double-click to install it
4. You may also need to install the Microsoft Visual C++ Redistributable if prompted

Option 3: Use PowerShell to install automatically
You can run this PowerShell command as administrator:
<code>
# Install winget via PowerShell
$progressPreference = 'silentlyContinue'
Invoke-WebRequest -Uri https://aka.ms/getwinget -OutFile Microsoft.DesktopInstaller.msixbundle
Add-AppxPackage Microsoft.DesktopInstaller.msixbundle
</code>

Option 4: Install via Chocolatey (if you have it)
<code>choco install winget</code>

After installation, restart your PowerShell/Command Prompt window and try running <code>winget --version</code> to verify it's working.

Would you like me to help you execute any of these installation methods?
