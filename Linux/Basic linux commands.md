# Basic linux commands 
[Back to linux page ](Linux.md)
- --
## Basic navigation and creation commands
pwd : print working directory
pwd 

cd : Change directory 
cd Desktop

ls : list files & directories
ls , ls -l , ls -la

touch : create file
touch hello.txt

cat : list content in file and join them
cat file1 , cat file1 file2 > file3 

echo : print statement
echo "Hello"

cp : copy file
cp test1.txt ./Desktop/files/test2.txt

mv : move file
mv test1.txt ./Desktop/files

mkdir : make directory
mkdir test , mkdir -p test1/test2/test2

rm : remove file
rm test.txt , rm -r directory

locate : find location of file
locate test*

find : find location of file in given directory
find test*

grep : show lines that consists word
grep "hello" file.txt , grep "hello"

- --
## Storage and files related commands
df : report on the system's disk space use 
df , df -m

du : disk usage shown in blocks
du , du -h , du -sh

free : check RAM usage
free , free -h

diff : compare contents of two files and display difference
diff file.txt test.txt

tar : convert into tarball or zip basically archiving
tar < options > files

zip : to zip files
zip files

unzip : to unzip files
zip file.zip

gzip : to zip files
gzip files

gunzip : to unzip files
gzip file.zip

sort : sort list
sort file.txt

uniq : show unique words
uniq file.txt

wc : word count 
wc file.txt , wc -l file.txt

scp : opensssh secure shell file copy
scp file.txt 

cut : cut strings
cut -d "-" -f 2

ln : link for file
ln test.txt , ln -s test.txt

strings : sequence of printable characters in files
strings data.txt

gpg : encrypt and decrypt file
gpg file.txt.gpg , gpg file.txt

tac : reverse print file
tac file.txt > reverse.txt

stat : Information about file
stat file.txt

tr : translate
cat file.txt | tr -s '[a-z]' '[A-Z]'
- --
## Text editors and file viewing commands

head : view starting n lines of files
head file.txt , head -n 10 file.txt

tail : view last n line of file
tail file.txt , tail -n 10 file.txt

vi : vim editor
vi file.txt

nano : nano editor
nano file.txt

- --
## Permission of files
chmod : change permission of files (ls -la for permissions)
chmod ugo+rwx file.txt , chmod ugo-rwx file.txt  , chmod 777 file.txt 

chown : change ownership of file
chown root(user) file.tar

chgrp : change group ownership
- --
## Running processes commands

jobs : current jobs along with status
jobs

top : show running tasks i.e. linux task manager
top 

kill : kill process using PID from top
kill 123455 , kill -9(SIGTERM) PID , kill -15(SIGKILL) PID

ps : return running process status
ps , ps aux

fg : get process to foreground
fg id

bg : get process in background
bg
- --
## System related commands 

systemctl : start , stop or check status of service
systemctl start ssh

journalctl : logs about service
journalctl -u ssh.service

service : run a System V init script
service name start , service tor stop

xargs : pass list as input
cat filenames.txt | xargs rm

- --
## Users , system and group commands 

uname : Unix name , details about system
uname , uname -a , uname -r

useradd : add users 
useradd user

userdel : delete user
userdel Username , userdel -r username

usermod : Modifies a user account , add user to group
usermod user

passwd : change password
passwd

whoami : displays username
whoami

who : currently logged in users
who 

groups : check which group user belongs to
groups root , groups user

groupadd : add group
groupadd group_name

id : returns user identity
id 

hostname : name of host i.e. user
hostname , hostname -i 

env : prints environment or sets and executes command
env

chsh : change login shell
chsh

sudo : super user do
sudo -s , sudo apt-get install python3

su : change user in shell , switch user
su user

visudo : sudoers list can be edited
visudo

- --
## Help and info about commands
man : manual page
man nmap , man ls

apropos : description about tools
apropos sudo

whatis : simple description
whatis cd

- --
## Commands not to specific
clear : clear terminal window
clear / ctrl + l

history : shows commands that you ran
history

- --
## Devices attached commands
lsblk : Lists block devices.
lsblk

lsusb : Lists USB devices
lsusb

lsof : Lists opened files.
lsof

lspci : Lists PCI devices.
lspci
- --
## Package manager (List)
dpkg : The dpkg is a tool to install, build, remove, and manage Debian packages. The primary and more user-friendly front-end for dpkg is aptitude.

apt : Apt provides a high-level command-line interface for the package management system.

aptitude : Aptitude is an alternative to apt and is a high-level interface to the package manager.

snap : Install, configure, refresh, and remove snap packages. Snaps enable the secure distribution of the latest apps and utilities for the cloud, servers, desktops, and the internet of things.

gem : Gem is the front-end to RubyGems, the standard package manager for Ruby.

pip : Pip is a Python package installer recommended for installing Python packages that are not available in the Debian archive. It can work with version control repositories (currently only Git, Mercurial, and Bazaar repositories), logs output extensively, and prevents partial installs by downloading all requirements before starting installation.

git : Git is a fast, scalable, distributed revision control system with an unusually rich command set that provides both high-level operations and full access to internals.

- --
## Running commands in sequence
; 
ls ; pwd
Even with errors all commands run independently

&&
ls && pwd
Stop if error i.e all commands are related

|
ls | pwd
depends upon previous process and error free execution
- --
### Sources : 
- [Hak5 series](https://www.youtube.com/watch?v=b5NmtmNwMgU&list=PLW5y1tjAOzI2ZYTlMdGzCV8AJuoqW5lKB&ab_channel=Hak5)
- [ProgrammingKnowledge youtube series](https://www.youtube.com/playlist?list=PLS1QulWo1RIb9WVQGJ_vh-RQusbZgO_As) 