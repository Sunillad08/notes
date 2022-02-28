# Basic commands
[Back to windows page](./index.md)

---

## CMD vs Powershell
Command prompt or cmd is a default application of windows that are used to interact with any windows objects in the windows os.
PowerShell is a more advanced version of cmd. It is not only an interface but also a scripting language that is used to carry out administrative tasks more easily.

---

## CMD

## Basic commands
 cd : change directory
 cd /Documents
 
 dir : list file and directories in folder
 dir
 
 rename : rename file
 rename c: old.txt new.txt
 
 help : show help for command
 help commandname /?
 
 Stop-Process : stop process
 Stop-Process -Name “ProcessName”
 
 shutdown : shutdown system
 shutdown /s , shutdown /r
 
 ipconfig : show ip configurations
 ipconfig 
 
 cls : clear terminal
 cls
 
 cmd : start cmd
 cmd
 
 powershell : start powershell
 powershell
 
 date : show date
 date

---

## CMD

## Basic commands
 Set-Location : change directory -> cd
 Set-Location /Documents
 
 Get-Childitem : list fire and directories in folder -> dir , ls
 Get-Childitem /Documents
 
 rename : rename file -> rename
Rename-Item “c:file.txt” -NewName “new.txt”

Get-Help : show help for command -> man , help
Get-Help “Cmdlet name”

Stop-Process : stop process
Stop-Process -Name “ProcessName”

Stop-Computer : shutdown system
Stop-Computer

Restart-Computer : Restart computer
Restart-Computer

Test-Connection : show ip configuration -> ipconfig
Test-Connection -ComputerName (hostname)

 cmd : start cmd
 cmd
 
 powershell : start powershell
 powershell
 
 date : show date
 date
 
---

### Source
- [cmd vs psh video](https://youtu.be/H0gwnFV_SFs)
- [cmd vs psh website](https://www.educba.com/powershell-vs-command-prompt/)
- https://12ft.io/proxy?q=https://www.thomas-krenn.com/en/wiki/Cmd_commands_under_Windows