# Windows-Inv_script
Windows Inv_script - A PowerShell-based forensic artifact collector that automatically gathers system information, logs, and security data from Windows devices for incident response and system analysis. Features automated collection of autoruns, processes, network connections, event logs, and more into a single organized report.


## Features

Collects the following artifacts:
- Autoruns
- Installed Programs
- Network Connections
- Prefetch Files
- Running Processes
- Scheduled Tasks
- Security Event Logs
- Services
- SMB Sessions
- System Information
- Temp Directories Content
- Users and Groups
- Windows Defender Support Logs

## Requirements

- Windows Operating System
- PowerShell 5.1 or higher
- Administrative privileges

## Installation

1. Clone this repository:
```powershell
git clone https://github.com/schvilum/windows-inv_script.git
```

2. Navigate to the tool directory:
```powershell
cd windows-investigation-tool
```

## Usage

1. Open PowerShell as Administrator
2. Set execution policy (if needed):
```powershell
Set-ExecutionPolicy RemoteSigned
```

3. Run the script:
```powershell
.\src\Invoke-Investigation.ps1
```

The script will create a directory named `Investigation_[timestamp]` in the C:\ drive containing all collected artifacts.

## Output

The tool generates a single text file containing all collected information, organized into clearly marked sections. The file is saved as:
```
C:\Investigation_[timestamp]\investigation.txt
```

## Security Considerations

- This tool collects sensitive system information. Handle the output with appropriate security controls
- Review collected data before sharing to ensure no sensitive information is exposed
- Run the tool only on systems you have authorization to investigate
