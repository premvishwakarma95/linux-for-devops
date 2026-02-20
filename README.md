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
- `df -h` - command to check disk usage i mean disk info
- `free -h` - command to check Ram usage

---

## File management and Common Commands
- `date` - command to know date in terminal
- `ls` - command to show list folder whatever inside existing directory
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
-  1 hour 6 minits
