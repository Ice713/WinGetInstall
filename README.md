# WinGetInstall
Install WinGet on PC (like Win 10 or older versions)

How to install winget on Win10 PC that doesn't recognize winget?<br>
To install winget on a Windows 10 PC that doesn't recognize the winget command, you have several options:

<h3>Option 1: Install from Microsoft Store (Recommended)</h3>
1. Open Microsoft Store<br>
2. Search for "App Installer"<br> 
3. Install or update the "App Installer" app<br>
4. Winget comes bundled with App Installer<br>

<h3>Option 2: Download from GitHub</h3>
1. Go to the winget GitHub releases page: <a href="https://github.com/microsoft/winget-cli/releases">https://github.com/microsoft/winget-cli/releases</a><br>
2. Download the latest <code>.msixbundle</code> file<br>
3. Double-click to install it<br>
4. You may also need to install the Microsoft Visual C++ Redistributable if prompted<br>

<h3>Option 3: Use PowerShell to install automatically</h3>
You can run this PowerShell command as administrator:<br>
<code>
# Install winget via PowerShell
$progressPreference = 'silentlyContinue'
Invoke-WebRequest -Uri https://aka.ms/getwinget -OutFile Microsoft.DesktopInstaller.msixbundle
Add-AppxPackage Microsoft.DesktopInstaller.msixbundle
</code>

<h3>Option 4: Install via Chocolatey (if you have it)</h3>
<code>choco install winget</code>

After installation, restart your PowerShell/Command Prompt window and try running <code>winget --version</code> to verify it's working.<br>

Would you like me to help you execute any of these installation methods?
