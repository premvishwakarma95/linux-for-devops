# Linux for devops

## Roadmap for devops

###  with shubham (this is a channgel name) -> learn these below things from this channgel

### Check the below roadmap
### Linux -> shell scripting -> networking basics -> github -> docker -> kubernnetives -> jenkins -> Argo cd -> prometheus, graphana -> aws

## PM2 commands
- pm2 start npm --name "alzato" -- run start  // start and create service name
- pm2 start index.js --name "alzato"
- pm2 list
- pm2 logs alzato

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

---

## About ssh.
It stands for secure shell. ssh port will always be 22. this is a way to access vps virtual private server. SSH uses keys to connect to with server ssh command uses private key and EC2 intance will have public key so with the help of these key we can connect.
```bash
ssh -i private-key.pem ubuntu@56.7.8.4.3
# 56.7.8.4.3 - this is a private ip of ec2 instance
```

---

## system-level commands
`uname` - It stands for Unix Name. by default it show kernal name, in linux show linux or in mac show darwin.
`uptime` - command to know how much time has system been up or open.
`who` - this command will tell which has loggedin and how many users and at what time they logged in.
`whoami` - this command will tell current logged in user in terminal and tells user name.
`which bash` - this command will tell which bash i am using like \usr\bin\bash this folder bash i am using this command tells this. I mean tell file path of that thing.
`which cp` - same as above command so `which` command is used to know about thing it could be anything.
`id` - this command will tell login user id and group id of current login user.
`sudo` - it is a group which has permission to do crazy things that's a sudo.
`sudo shutdown` - Command to shutdown the system. Instance would be stopped by this command.
2:15
