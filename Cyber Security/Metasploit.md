# Metasploit
[Back to cyber security page](Cyber%20security.md)
- --
## What is metasploit?
The **Metasploit** Project is a computer security project that provides information about security vulnerabilities and aids in penetration testing and IDS signature development. It is owned by Boston, Massachusetts-based security company Rapid7.

Its best-known sub-project is the open-source Metasploit Framework, a tool for developing and executing exploit code against a remote target machine. Other important sub-projects include the Opcode Database, shellcode archive and related research.

The Metasploit Project includes anti-forensic and evasion tools, some of which are built into the Metasploit Framework. Metasploit is pre-installed in the Kali Linux operating system. - Wikipedia 

The [Metasploit Framework](https://github.com/rapid7/metasploit-framework) (MSF) is far more than just a collection of exploits–it is also a solid foundation that you can build upon and easily customize to meet your needs.
- --
## Architecture
![Metasploit architecture|700](https://www.offensive-security.com/wp-content/uploads/2015/04/msfarch2.png)
- --
## File system
![Msf file system|700](https://www.offensive-security.com/wp-content/uploads/2018/05/msfu-lib0-1.png)

- DATA : The data directory contains editable files used by Metasploit to store binaries required for certain exploits, wordlists, images, and more.
- DOCUMENTATION : As its name suggests, the documentation directory contains the available documentation for the framework.
- LIB : The lib directory contains the ‘meat’ of the framework code base
- MODULES : The modules directory is where you will find the actual MSF modules for exploits, auxiliary and post modules, payloads, encoders, and nop generators.
- PLUGINS : As you will see later in this course, Metasploit includes many plugins, which you will find in this directory.
- SCRIPTS : The scripts directory contains Meterpreter and other scripts.
- TOOLS : The tools directory has various useful command-line utilities.

- --
## METASPLOIT MODULES AND LOCATIONS
In the Metasploit Framework, _exploit_ modules are defined as modules that use payloads.
Auxiliary modules include port scanners, fuzzers, sniffers, and more. Payloads consist of code that runs remotely, while encoders ensure that payloads make it to their destination intact. Nops keep the payload sizes consistent across exploit attempts. If you need to load additional modules from with msfconsole, use the loadpath command.

In the Metasploit Framework, all modules are Ruby classes.

-   _Modules_ inherit from the type-specific class
-   The type-specific class inherits from the Msf::Module class
-   There is a shared common API between modules

_Payloads_ are slightly different.

-   Payloads are created at runtime from various components
-   Glue together stagers with stages

- --
## msfconsole
msfconsole is console version to use metasploit.
Here are basic commands :
```bash
back          Move back from the current context
banner        Display an awesome metasploit banner
cd            Change the current working directory
color         Toggle color
connect       Communicate with a host
edit          Edit the current module with $VISUAL or $EDITOR
exit          Exit the console
get           Gets the value of a context-specific variable
getg          Gets the value of a global variable
go_pro        Launch Metasploit web GUI
```
```bash
grep          Grep the output of another command
help          Help menu
info          Displays information about one or more module
irb           Drop into irb scripting mode
jobs          Displays and manages jobs
kill          Kill a job
load          Load a framework plugin
loadpath      Searches for and loads modules from a path
makerc        Save commands entered since start to a file
popm          Pops the latest module off the stack and makes it active
```
```bash
previous      Sets the previously loaded module as the current module
pushm         Pushes the active or list of modules onto the module stack
quit          Exit the console
reload_all    Reloads all modules from all defined module paths
rename_job    Rename a job
resource      Run the commands stored in a file
route         Route traffic through a session
save          Saves the active datastores
search        Searches module names and descriptions
sessions      Dump session listings and display information about sessions
check         Check if target is vulnerable to exploit
```
```bash
set           Sets a context-specific variable to a value
setg          Sets a global variable to a value
show          Displays modules of a given type, or all modules
sleep         Do nothing for the specified number of seconds
spool         Write console output into a file as well the screen
threads       View and manipulate background threads
unload        Unload a framework plugin
unset         Unsets one or more context-specific variables
unsetg        Unsets one or more global variables
use           Selects a module by name
version       Show the framework and console library version numbers
```
- --
## Payload
A payload in Metasploit refers to an exploit module. There are three different types of payload modules in the Metasploit Framework: Singles, Stagers, and Stages.

- **Singles** are payloads that are self-contained and completely standalone. A Single payload can be something as simple as adding a user to the target system or running calc.exe.
- **Stagers** setup a network connection between the attacker and victim and are designed to be small and reliable. It is difficult to always do both of these well so the result is multiple similar stagers. Metasploit will use the best one when it can and fall back to a less-preferred one when necessary.
- **Stages** are payload components that are downloaded by Stagers modules. The various payload stages provide advanced features with no size limits such as Meterpreter, VNC Injection, and the iPhone ‘ipwn’ Shell.

- --
## Database in metasploit
When conducting a penetration test, it is frequently a challenge to keep track of everything you have done on (or to) the target network. This is where having a database configured can be a great timesaver. Metasploit has built-in support for the PostgreSQL database system.

Database Backend Commands : 

```bash
db_connect        Connect to an existing database
db_disconnect     Disconnect from the current database instance
db_export         Export a file containing the contents of the database
db_import         Import a scan result file (filetype will be auto-detected)
db_nmap           Executes nmap and records the output automatically
db_rebuild_cache  Rebuilds the database-stored module cache
db_status         Show the current database status
hosts             List all hosts in the database
loot              List all loot in the database
notes             List all notes in the database
services          List all services in the database
vulns             List all vulnerabilities in the database
workspace         Switch between database workspaces
```

Setup Metasploit database :
1. systemctl start postgresql
2. msfdb init
3. db_status

Issuing the ```workspace``` command from the msfconsole, will display the currently selected workspaces. The ‘default‘ workspace is selected when connecting to the database, which is represented by the * beside its name.

Adding workspace : ```workspace -a lab4```
Removing workspace : ```workspace -d lab4```
- --
## Meterpreter
**Meterpreter**, the short form of Meta-Interpreter is an advanced, multi-faceted payload that operates via dll injection. The Meterpreter resides completely in the memory of the remote host and leaves no traces on the hard drive, making it very difficult to detect with conventional forensic techniques. Scripts and plugins can be loaded and unloaded dynamically as required and Meterpreter development is very strong and constantly evolving.

### HOW METERPRETER WORKS
- The target executes the initial stager. This is usually one of bind, reverse, findtag, passivex, etc.
- The stager loads the DLL prefixed with Reflective. The Reflective stub handles the loading/injection of the DLL.
- The Metepreter core initializes, establishes a TLS/1.0 link over the socket and sends a GET. Metasploit receives this GET and configures the client.
- Lastly, Meterpreter loads extensions. It will always load stdapi and will load priv if the module gives administrative rights. All of these extensions are loaded over TLS/1.0 using a TLV protocol.

METERPRETER COMMANDS :

```bash
background      Send the current Meterpreter session to the background and return ‘msf’
clearev         Clear the Application, System, and Security logs on a Windows system
download        Downloads a file from the remote machine.
pwd             print working directory
cd              change directory
cat             display content of file
execute         execute command on target
getuid          display the user that the Meterpreter server is running as on the host
hashdump        post module will dump the contents of the SAM database.
ipconfig        displays the network interfaces and addresses on the remote machine
lpwd            display local working directory
lcd             change the local working directory
ls              list files in current working directory
ps              show running processes on the target 
search          locating specific files on the target host
shell           standard shell on the target
upload          uploads file on remote machine
webcam_list     display currently available web cams on the target host
webcam_snap     grabs a picture from a connected web cam on the target system
```
- --
## Information gathering in metasploit
db_nmap command to run [nmap](nmap.md) against our targets and our scan results would than be stored automatically in our database.

Metasploit has many more port scanners located in  auxiliary/scanner/.
- --
## Components in Metasploit
- Auxiliary: Any supporting module, such as scanners, crawlers and fuzzers.
- Encoders: Encoders will allow you to encode the exploit and payload in the hope that a signature-based antivirus solution may miss them.
- Evasion: While encoders will encode the payload, they should not be considered a direct attempt to evade antivirus software. 
- Exploits: Exploits, neatly organized by target system.
- NOPs: NOPs (No OPeration) do nothing, literally. 
- Payloads: Payloads are codes that will run on the target system. 
- Post: Post modules will be useful on the final stage of the penetration testing process listed above, post-exploitation.
- --
## Ranking modules
![Ranking in msf|700](https://tryhackme-images.s3.amazonaws.com/user-uploads/603df7900d7b6f1dff18b0bd/room-content/a88c8d37283878e01447853a68578deb.png)
- --
## Many more ..
There are many more applications of metasploit , check official website , Youtube playlist for more.
- --
### Source
- [offensive security metasploit](https://www.offensive-security.com/metasploit-unleashed/)
- [Hackersploit playlist](https://youtube.com/playlist?list=PLBf0hzazHTGN31ZPTzBbk70bohTYT7HSm)