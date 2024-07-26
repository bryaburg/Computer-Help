
# Computer Help

## Virtualbox

### Enable Nested Virtualization

Use these commands:

```shell
cd C:\Program Files\Oracle\VirtualBox
VBoxManage.exe list vms
VBoxManage.exe modifyvm "GNS3 VM" --nested-hw-virt on
```

## Print to Printer

```shell
type <file_to_print> | telnet <printer_ip> 9100
```

## Get Public IP Address

```shell
curl daveeddy.com/ip
```

## Google Dork Books

```shell
site:drive.google.com "Movie or book"
doctype:pdf "Book"
```

## Windows Product Key

```shell
wmic path softwareLicensingService get OA3xOriginalProductKey
```

## Task Manager Shortcut

```shell
Control + Shift + ESC
```

### Restore Explorer

1. Task Manager
2. Run new task
3. `explorer.exe`

## CMD Shortcuts

### Windows 10 Password Change

```shell
net user [username] [new password]
```

### System Scan

```shell
sfc /scannow
```

System scan to make sure they are working fine. Fixes Windows setup and recovery.

### See Connections to Outside PC

```shell
netstat -ano | findstr "ESTABLISHED"
wmic process where processid=xxxx get ExecutablePath
```

Retrieves the executable path of a specific process given its Process ID.

### Upgrade All Installed Applications

```shell
winget upgrade --all
```

Uses the Windows Package Manager (winget) to upgrade all installed applications.

### Windows Memory Diagnostic Tool

```shell
mdsched
```

Launches the Windows Memory Diagnostic tool to check for memory problems.

### System File Checker Tool

```shell
sfc /scannow
```

Runs the System File Checker tool to scan and repair corrupted system files.

### Check Health of Windows Image

```shell
DISM /Online /Cleanup /CheckHealth
DISM /Online /Cleanup /ScanHealth
DISM /Online /Cleanup /RestoreHealth
```

Checks the health of the Windows image to see if any corruption is present, scans the Windows image for corruption, and repairs the Windows image if corruption is detected.

### List All Running Processes

```shell
tasklist
```

### Terminate Running Processes

```shell
taskkill
```

### Generate Wireless Network Report

```shell
netsh wlan show wlanreport
```

### Display Network Interfaces Information

```shell
netsh interface show interface
netsh interface ip show address | findstr “IP Address”
netsh interface ip show dnsservers
```

Displays information about the network interfaces on the system, the IP addresses of network interfaces, and the DNS servers for the network interfaces.

### Windows Firewall Control

```shell
netsh advfirewall set allprofiles state off
netsh advfirewall set allprofiles state on
```

Turns off/on the Windows Firewall for all profiles.

### Network Tools

```shell
pathping
ping -a
ping -t
tracert
tracert -d
netstat
netstat -af
netstat -o
netstat -e -t 5
route print
route add
route delete
```

Various network diagnostic and troubleshooting commands.

### Restart Computer and Open Advanced Boot Options

```shell
shutdown /r /o
```

### IP Configuration

```shell
ipconfig /release
ipconfig /renew
```

Releases and renews the current IP address for all network adapters.

### Windows Memory Diagnostic

```shell
mdsched
```

## PowerShell Debloating

```powershell
iwr -useb https://christitus.com/win | iex
```

Software to help with debloating Windows.

### Check if Running as Administrator in PowerShell

```powershell
(New-Object Security.Principal.WindowsPrincipal([Security.Principal.WindowsIdentity]::GetCurrent())).IsInRole([Security.Principal.WindowsBuiltInRole]::Administrator)
```
