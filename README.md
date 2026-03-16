# Linux for devops

## Roadmap for devops

###  with shubham (this is a YouTube channgel name) -> learn these below things from this channgel

### Check the below roadmap
### Linux -> shell scripting -> networking basics -> github -> docker -> kubernnetives -> jenkins -> Argo cd -> prometheus, graphana -> aws services

## PM2 commands
- pm2 start npm --name "alzato" -- run start  // start and create service name
- pm2 start index.js --name "alzato"
- pm2 list
- pm2 logs alzato
- pm2 status
- pm2 kill
- pm2 stop all
- pm2 delete service_name

---

## What is linux?
- It is an OS.
  
## Ways to use Linux?
- WSL - (Windows subsytem for linux)
- Virtual box
- Buy VPS in aws or azure select linux os then use that.
- Install Vagrant, it's a software that will allow you to run linux.

## Steps to install WSL (Ubuntu) in window.
Step 1: Check Windows Version
```powershell
Win + R → type winver → Enter
```
Make sure:
- Windows 10 version 2004 or higher
- OR Windows 11 (recommended)
Step 2: Install WSL (One Command Method – Recommended)
- Open PowerShell as Administrator and run:
```bash
wsl --install
```
That’s it. This will:
- Enable required features
- Install WSL 2
- Install Ubuntu
- Set WSL 2 as default
Then Restart your PC.

## Ways to access VM - (Virtual machine).
- SSH - (secure shell)
- RDP - (Remote desktop protocol)
- AnyDesk - (It's, i think a software to get access of any system remotely)

## What is kernel?
What is like a heart of the machine that has access of everything linux kernel name is Linux kernel. And kernel is written in C language so to talk wiht kernel se use shell. Shell is a termial with the help of this we interact with kernel. for example we want to say make directory to kernel use `mkdir` command.
- Application (Terminal) -> Shell -> Kernal -> Hardware

---

## Hardware basic commands.
- `top` - command to check cpu usage or process that are running
- `df` - command to check disk detail.
- `df -h` - command to check disk usage i mean disk info
- `free -h` - command to check Ram usage
- `nohup free -h` - this command will create file nohup.out and put all text or info that we get in editor inside nohup.out file. I mean we use this command to store logs of something.

---

## Basic File management Commands
- `date` - command to know date in terminal
- `ls` - command to show list folder whatever inside existing directory
- `ls -a` - this will also list hidden folders and hidden folder start wiht . (dot) .ssh like this
- `mkdir devops` - command will make directory with name devops
- `ls -l` - command will show directory with some info like when and who created and permissions in short it lists in detail.
- `pwd` - it stands for present working directory. command tell in which location you are i mean current location.
- `touch new_file.txt` - command to create file not folder file.
- `clear` - command to clear the terminal
-  `cd dirctory_name` - stands for change directory. command to go to any directory.
-  `cd ..` - command to back in previous directory.
-  `rm fileName.txt` - it stand for remove. Command to delete file. only you can delete one file.
-  `rm -r /devops` - Command to delete all things inside devops directory. and also remove devops directory and inside all files and directory.
-  `rmdir /devops` - Command to remove directory.
-  `cat newFile.txt` - command to read the content of a file.
-  `echo "hello dosto"` - command to print text in the termial.
-  `echo "hello dosto" > newFile.txt` - this command will write this hello dosto text inside file newFile.txt, even if newFile will not exist then create and write this code this is what this command does.
-  `zcat newfile.zip` - command to read file of zip file.
-  `head newFile.txt` - This command will print the first five lines of the file.
-  `tail newFile.txt` - This command will print the last five lines of the file.
-  `tail -f newFile.txt` - This command will print last lines and also the file will open if anything comes in file in last then it will print in realtime, press ctrl + c to exist the editor.
-  `cp newFile.txt devops/` - cp stands for copy. this command will copy newFile.txt to the devops folder.
-  `cp -r cloud devops/` - This command will copy cloud folder to devops folder.
-  `mv newFile.txt ../devops/` - mv stands for move. this command will move newFile.txt to devops folder.
-  `mv devops/ linux_for_devops` - this command will rename from devops to linux_for_devops.
-  `wc newFile.txt` - it stands for word count. result would be like this `1 4 16 newFile.txt` 1 is count of line, 4 word, 16 byte means size of file.
-  `ln -s /home/ubuntu/devops/newFile.txt soft-link` - this command will create soft link of this newfile.txt file means like we put desktop icon in desktop but it is stored in desktop just path or link and one more important thing if main file newfile.txt deleted then soft-link will be red and will have nothing means deleted too.
-  `ln /home/ubuntu/devops/newFile.txt hard-link` this will create hard link file with name hard-link and will not be deleted if we delete main file.
-  `cut -b 1-4 newFile.txt` - this command will print 1 to 4 byte content from file -b stands for byte and as we know one character is of 1 byte in string.
- `diff hello.txt newFile.txt` - This command will show the difference between these two file. i mean text.

---

## There are two editor for linux command line Vi, vim editor and nano editor.
### vi and vim editor both are same.
command to open file and editor file using vi editor.
```bash
vi hello.txt
```
This command will open hello.txt file and click `i` button to insert text or edit file, if want to come out from insert mode click `escape` button. click `: and write wq` and enter this will close the editor. `:` then `wq`.

### nano editor.
```bash
nano file.txt
```
This command will open file.txt in editor after editing press `ctrl + 0` then click `Enter button` this will save and then `ctrl + X` this will close the editor.

---

## About ssh.
It stands for secure shell. ssh port will always be 22. this is a way to access vps virtual private server. SSH uses keys to connect to with server ssh command uses private key and EC2 intance will have public key so with the help of these key we can connect.
```bash
ssh -i private-key.pem ubuntu@56.7.8.4.3
# 56.7.8.4.3 - this is a private ip of ec2 instance
```

---

## system-level commands
- `uname` - It stands for Unix Name. by default it show kernal name, in linux show linux or in mac show darwin.
- `uptime` - command to know how much time has system been up or open.
- `who` - this command will tell which has loggedIn and how many users and at what time they logged in.
- `whoami` - this command will tell current loggedIn user in terminal and tells user name.
- `which bash` - this command will tell which bash i am using or where bash exactly is i mean path like \usr\bin\bash this folder bash i am using this command tells this. I mean tell file path of that thing.
- `which cp` - same as above command so `which` command is used to know about thing it could be anything.
- `id` - this command will tell login user id and group id of current login user.
- `sudo` - It lets a permitted user run commands as root (admin). it is a group which has permission to do crazy things that's a sudo.
- `sudo shutdown` - Command to shutdown the system. Instance would be stopped by this command.
- `sudo su` - switch from normal user to root user and if want to back to normal user use `exit` command.
- `exit` - command to back from root user to normal user that were logged in before `sudo su` command.
- `sudo reboot` - this command will reboot your system means ec2 instance.

---

### what is `apt` in linux?
apt is a commandline application package manager. And you can run apt command with the help of sudo only because super user only have access to install package and manage package that's why.

```bash
sudo apt insatll docket.io
// this will install docker.io if available in the system. i mean will try to find in systme in that we are running this command
sudo apt-get install docker.io
// this apt-get will try to install from all over the internet so this is a difference between apt and apt-get.
```

common commands of apt.
- `sudo apt-get udpate` - command to udpate system. now system has all security and all udpated thing.
- `sudo apt-get docker.io` - command to install docker.
- `sudo apt remove docker.io` - command to remove docker from system.
- `which docker` - command to know where docker is in system or in direcotry. this will tell /usr/bin/docker

So this is apt and what it does.

---

## User and file management.
If you will run permission command without sudo then it will give error.

User and group management commands
- `sudo useradd -m jethalal` - command to add user. this command will add jethalal user and -m make directory of that user name /home/jethalal.
- `sudo passwd jethalal` - command to add password for jethalal user.
- `su jethalal` - command to switch from ubuntu to jethalal.
- `sudo userdel jethalal` - command to delete user jethalal.
- `cat /etc/passwd` - command to see the list of users.
- Whenever we will create user then group will also be created with same of the user and if we install docker then docker name group also be created.
- `sudo groupadd developers` - command to add group.
- `sudo gpasswd -a jethalal developers` - command to add jethalal to developers group -a stand for add.
- `sudo gpasswd -M iyer,tappu,bhide developers` - command to add multiple user in the group -M stand for multiple.
- `sudo groupdel developers` - command to delete group like here we are deleting developers group.
- `cat /etc/group` - command to see the list of groups.

### File permission commands
- `ls -l` - command to see the file and directory with file permission.
- `chmod 777 devops` - command to change the permission of directory. so here chmod is command to change permission, 777 is permission, devops is a directory name.
- when i this `ls -l` then i got this `drwxrwxr-x 2 ubuntu ubuntu 4096 Feb 18 18:14 devops` so here this is permision of folder devops. when permission start with `d` it means it's a directory and we break this permission `drwxrwxr-x` in three pair like d means directory `rwx` first three pair means user, second pair `rwx` means group, and third pair means `r-x` other user. `r` means read, `w` means write, `x` means execute.
- check below table to understand correctly
Linux File Permission Values

| Permission | Value |
|------------|-------|
| --- | 0 |
| --x | 1 |
| -w- | 2 |
| -wx | 3 |
| r-- | 4 |
| r-x | 5 |
| rw- | 6 |
| rwx | 7 |

Permission Meaning
- **r** = Read (4)
- **w** = Write (2)
- **x** = Execute (1)
Example -
(command to change the file permission)
```bash
chmod 755 file.sh
```
**Explanation:**
- 7 → rwx (Owner)
- 5 → r-x (Group)
- 5 → r-x (Others)
- 3:03 hours video stop time

### Change ownership of the file
```bash
// chown - means change owner and jethalal is a user.
sudo chown jethalal demoFile.txt
```
this command will now make jethalal the owner of demoFile.txt

### change group of the file.
```bash
// chgrp - change group and devops is the group
sudo chgrp devops demoFile.txt
```

---

## Compression command means making zip in server.
- First install the `zip` package. This package will zip the cloud files.
- `sudo apt install zip`
- commadn to zip the file
- `zip -r backup.zip frontend/` - here zip is package, -r for recursively, backup.zip is the name of zip that we are creating, frontend/ is folder name inside this folder all the file will be in zip now.
- Command to unzip the zip file.
- `unzip backup.zip` - this will unzip the zip file.

---

## Command to transfer or copy file from local to you ec2 server and from ec2 to local.
scp stand for secure copy.
```bash
scp -i private-key.pem app.zip ubuntu@56.7.8.4:/home/ubuntu/
```
scp stand for secure copy, app.zip is file of our local system and copying in home/ubuntu folder. And app.zip is in current directory that why we are using app.zip.
```bash
scp -i private-key.pem ubuntu@56.7.8.4:/path/to/ec2/file /path/to/local/folder
```
This command will copy file from EC2 to our local machine.

---

## Networking commands.
- ping stand for `Packet InterNet Groper`. ping command check is website working or also show the ip address of the vps and check internet working or not.
```bash
ping ibrcloud.com
```
- `netstat` stand for network statistics. In simple terms, netstat shows what network connections your computer or server currently has.
```bash
netstat
```
- `ifconfig` stands for Interface Configuration. It helps you see IP address, MAC address, network status, and traffic information of your system.
```bash
ifconfig

// Output of the command
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>
inet 172.31.25.10
netmask 255.255.255.0
ether 02:7b:64:1a:3f:21
```
- `traceroute` - This will tell how we get interact and get data from any server. this show all the networks. if we request for google.com then first it will go to network provider server then DNS then it send to the ip of the server then google then google will give response and response will come to the user and all this networks comes this command shows these networks.
```bash
traceroute google.com

// Output- This will show every network hop between your machine and the Google server.
1  192.168.1.1      1.123 ms
2  10.0.0.1         5.342 ms
3  172.217.160.78   18.234 ms
```
- `tracepath` - same as traceroute.
```bash
tracepath google.com
```
- `mtr` stand for My Traceroute. If we want to get info of these two commands `ping` and `tracepath` then run only `mtr` this will give info of both commands.
```bash
mtr google.com
```
- `nslookup` stands for Name Server Lookup. Find IP Address of a Domain
```bash
nslookup google.com

output -
Server:  8.8.8.8
Address: 8.8.8.8#53

Non-authoritative answer:
Name:    google.com
Address: 142.250.183.46

// DNS server used: 8.8.8.8
// google.com resolves to 142.250.183.46
```
- `hostname` - this command will the hostname of the server.
```bash
hostname
// this command will show the all host of the server
cat /etc/host
```
- `ip address show` - command to show ip address and network ip.
- `iwconfig` - command to show wireless network ips.
- `whois google.com` - command to show all things about domain like domain name, registy domain, register url, created date, udpate date, which server.

## General networking commands that we use.
- `curl` - command to call api end points.
```bash
curl https://jsonplaceholder.typicode.com/posts
```
- `wget` - command to download anything from internet.
```bash
wget https://file-example.com/file.jpg
```
- `watch` - command to run anything in every two second.
```bash
watch top

// command with given time, in every 5 second.
watch -n 5 top
```
- `nmap -v google.com` - command to scan the server, check is there any port is open or not.

---

## Pro linux commands.
what is awk?
- `awk` is a powerful text-processing command-line tool in Linux/Unix used to search, filter, and manipulate text or data in files. In awk data should be formatted like csv comma separated or tsv tab separated value.
```bash
awk '/INFO/ {count++} END {print "The count of INFO IS", count}' app.log
```
What it does
- /INFO/ → searches for lines containing INFO
- {count++} → increments a counter for each match
- END {print ...} → after reading the whole file, prints the count
- app.log → the log file being analyzed
Output example
```bash
The count of INFO IS 16
````
✅ This command counts how many times "INFO" appears in app.log.

---

What is `sed`?
- `sed` stands for Stream Editor. It is a Linux command used to search, replace, delete, or modify text in a file or stream of data without opening the file in an editor. 🧑‍💻
- Example
```bash
sed 's/hello/hi/' file.txt
```
Output - This replaces the first occurrence of "hello" with "hi" in each line.

---

What is `grep`?
`grep` is a Linux command used to search for specific text or patterns inside files. 🔍
```bash
grep ERROR app.log
```
- This prints all lines containing ERROR in app.log.
Example output:
```bash
2026-03-12 ERROR Database connection failed
```

---

## Linux volume management.
### `lsblk` stands for List Block Devices.
It will show all the EBS that attached to this connected EC2. It is a Linux command used to display information about storage devices such as:
- Hard disks
- SSDs
- USB drives
- Partitions
- Mounted volumes
It shows the structure of disks and partitions in a tree format. 💾
```bash
lsblk
```
Example output:
```bash
NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
xvda    202:0    0   20G  0 disk
├─xvda1 202:1    0   19G  0 part /
└─xvda2 202:2    0    1G  0 part [SWAP]
```

### command to know free disk or space.
```bash
df -h
````
Output
```bash
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       20G   12G   7G   64% /
tmpfs           487M     0  487M   0% /dev/shm
/dev/xvdf       100G   20G   80G  20% /data
```

### `LVM` (logical volume manager).
Learn about when you need to add more space to the server at that time you need to create EBS then attache to EC2 then make it usable at that time you use it.
