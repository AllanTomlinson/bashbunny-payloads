# Ducky Script Template for Bash Bunnys

Author: @kevthehermit
Version: Version 1.1

## Description

Boiler Plate for running ducky scripts on the Bash Bunny

Disable TP (Tamper Protection) on Win 10 anti virus.  
Launch Powershell as Administrator.  
Roll back Win 10 Defender AV definitions to "none".  
Need to disable Real Time Protection too, try:
`MpCmdRun.exe" -RemoveDefinitions -All Set-MpPreference -DisableIOAVProtection $true`
Then run laZagne.exe All

## Configuration

HID or HID STORAGE

## Requirements

Install DuckToolkit payload for extra language support

## STATUS

| LED                                              | Status                      |
| ------------------------------------------------ | --------------------------- |
| Magenta solid                                    | Setup                       |
| Yellow single blink                              | Script Running (Attack)     |
| Green 1000ms VERYFAST blink followed by SOLID    | Finished                    |
