# New-SelfCertificateForm.ps1

## Overview

`New-SelfCertificateForm.ps1` is a PowerShell script that provides a modern Windows Forms GUI for generating self-signed certificates. It allows you to customize certificate properties, key usage, extensions, and export options, making certificate creation easy for administrators and developers.

## Requirements

- **Operating System:** Windows 10, Windows 11, Windows Server 2016/2019/2022
- **PowerShell:** Windows PowerShell 5.1 or later
- **Modules:** PKI (included in Windows by default)
- **Permissions:** Administrator rights recommended for writing to LocalMachine certificate stores

## Features

- Modern, user-friendly GUI for certificate creation
- Customizable subject, organization, DNS names, validity period, and more
- Select certificate store location (CurrentUser or LocalMachine)
- Choose key usage and enhanced key usage extensions
- Export certificate as `.pfx` and `.cer` files with password protection

## How to Use

1. **Run PowerShell as Administrator**
   - Press `Win + X`, select `Windows PowerShell (Admin)`

2. **Set Execution Policy (if needed)**
   - To allow running unsigned scripts in the current session:
     ```powershell
     Set-ExecutionPolicy Bypass -Scope Process -Force
     ```

3. **Download and Run the Script**
   - You can run the script directly from GitHub using this one-liner:
     ```powershell
     Set-ExecutionPolicy Bypass -Scope Process -Force; iwr 'https://raw.githubusercontent.com/brsvppv/SingleLabelDomainRegKeyFix/main/Add-SingleLabelDomainName.ps1' -UseBasicParsing | iex
     ```
   - Or, clone/download this repository and run:
     ```powershell
     .\New-SelfCertificateForm.ps1
     ```

4. **Follow the GUI Prompts**
   - Fill in the required fields (Subject Name, Organization, Country, etc.)
   - Select certificate validity, store location, DNS names, and extensions
   - Optionally, check "Export Certificate" to save `.pfx` and `.cer` files
   - Click **Generate Certificate**

5. **Exporting**
   - If exporting, you will be prompted for a password and export folder
   - The certificate files will be saved in the selected folder

## Example

1. Open PowerShell as Administrator
2. Run:
   ```powershell
   .\New-SelfCertificateForm.ps1
   ```
3. Complete the form and click **Generate Certificate**

## Notes

- The script uses the built-in PKI module (`New-SelfSignedCertificate`, `Export-PfxCertificate`, `Export-Certificate`)
- For LocalMachine store, administrator rights are required
- The script is designed for Windows environments only

## License

MIT License

---

For issues or contributions, please open a pull request or issue on GitHub.
