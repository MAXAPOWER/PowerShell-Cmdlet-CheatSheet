# PowerShell-Cmdlet-CheatSheet
MS PowerShell Cmdlets and Shortcuts (for when I inevitably forget some).

### Table of Contents
---

| No. | Topic                                            |
|-----|--------------------------------------------------|
|  1  | [**PoSh Cmdlets**](#posh-cmdlets)              |
|  2  | [**PoSh Aliases**](#posh-aliases)            |
|  3  | [**PoSh Variables**](#posh-variables)            |
|  4  | [**IO Redirection**](#io-redirection)            |
|  5  | [**Directory Operations**](#directory-operations)|
|  6  | [**Find Files**](#find-files)                |
|  7  | [**File Operations**](#file-operations)          |
|  8  | [**Process Management**](#process-management)    |

### PoSh Cmdlets

| Cmdlet | Description                               |
|---------|---------------------------------------|
| $PSVersionTable | Prints PS version          |
| (Get-Process powershell).path \| select -first 1 | Prints where PowerShell is executing from       |
| Test-ComputerSecureChannel -verbose | Tests trust relationship between LM and DC |
|

### Find Files

| Cmdlet | Description                               |
|---------|---------------------------------------|
| gci -Path \\..\\<fileName> -Recurse -Force -ErrorAction SilentlyContinue | Recursive search through all directories, ignoring errors from inaccessible paths          |
| gwmi -Class win32_product \| select Name,Version,Vendor \| sort name \| Export-Csv $home\Desktop\sw_list.csv -NoTypeInformation | Get SW list of installed apps/pkgs          |
|
