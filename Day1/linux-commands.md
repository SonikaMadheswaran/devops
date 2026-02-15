# 🚀 Linux Commands Reference Guide

![Linux](https://img.shields.io/badge/Linux-Ubuntu-E95420?style=for-the-badge&logo=ubuntu)
![Shell](https://img.shields.io/badge/Shell-Bash-4EAA25?style=for-the-badge&logo=gnubash)
![CLI](https://img.shields.io/badge/Interface-Command%20Line-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Level-Beginner%20to%20Advanced-success?style=for-the-badge)

---

# 📌 What is Linux?

Linux is an open-source operating system widely used in:

- ☁️ Cloud Computing
- 🖥️ Servers
- 🐳 Containers
- 🔐 Cybersecurity
- 🚀 DevOps Environments

Linux is primarily managed using the **Command Line Interface (CLI)**.

---

# 🧭 Basic Navigation Commands

## 📂 Check Current Directory
```bash
pwd
```

## 📁 List Files and Directories
```bash
ls
ls -l
ls -a
```

## 📂 Change Directory
```bash
cd foldername
cd ..
cd ~
```

## 📁 Create Directory
```bash
mkdir foldername
```

## ❌ Remove Directory
```bash
rmdir foldername
rm -r foldername
```

---

# 📄 File Management Commands

## 📄 Create File
```bash
touch filename.txt
```

## ✏️ Edit File
```bash
nano filename.txt
vi filename.txt
```

## 📖 View File Content
```bash
cat filename.txt
less filename.txt
more filename.txt
```

## 📋 Copy File
```bash
cp file1.txt file2.txt
```

## 🔁 Move / Rename File
```bash
mv oldname.txt newname.txt
```

## ❌ Delete File
```bash
rm filename.txt
```

---

# 🔍 Search & Filter Commands

## 🔎 Search for Files
```bash
find / -name filename
```

## 🔍 Search Inside File
```bash
grep "word" filename.txt
```

## 📊 Count Words
```bash
wc filename.txt
```

---

# 👤 User Management Commands

## ➕ Add User
```bash
sudo adduser username
```

## ❌ Delete User
```bash
sudo deluser username
```

## 🔑 Change Password
```bash
passwd username
```

## 👥 List Users
```bash
cat /etc/passwd
```

---

# 🔐 Permission Commands

## 🔎 Check Permissions
```bash
ls -l
```

## 🔑 Change Permissions
```bash
chmod 755 filename
```

## 👤 Change Ownership
```bash
chown user:group filename
```

Permission Format:

```
r = read (4)
w = write (2)
x = execute (1)
```

---

# 📦 Package Management (Ubuntu/Debian)

## 🔄 Update Packages
```bash
sudo apt update
```

## ⬆️ Upgrade Packages
```bash
sudo apt upgrade
```

## 📥 Install Package
```bash
sudo apt install package-name
```

## ❌ Remove Package
```bash
sudo apt remove package-name
```

---

# ⚙️ Process Management

## 📊 View Running Processes
```bash
ps
top
htop
```

## ❌ Kill Process
```bash
kill PID
kill -9 PID
```

---

# 🌐 Networking Commands

## 🌍 Check IP Address
```bash
ip a
ifconfig
```

## 📡 Test Connectivity
```bash
ping google.com
```

## 🌐 Check Open Ports
```bash
netstat -tulnp
```

## 🔎 Check DNS
```bash
nslookup google.com
```

---

# 💾 Disk Management

## 💽 Check Disk Usage
```bash
df -h
```

## 📂 Check Folder Size
```bash
du -sh foldername
```

---

# 📦 Archive & Compression

## 📦 Create Tar File
```bash
tar -cvf archive.tar foldername
```

## 📂 Extract Tar File
```bash
tar -xvf archive.tar
```

## 🗜️ Compress with Gzip
```bash
gzip filename
```

---

# 🔄 Useful Shortcuts

| Shortcut | Description |
|----------|------------|
| Ctrl + C | Stop process |
| Ctrl + Z | Suspend process |
| Ctrl + L | Clear screen |
| Tab | Auto-complete |
| history | Show command history |

---

# 🎯 Why Linux Commands Matter in DevOps?

✅ Essential for Cloud Servers  
✅ Required for CI/CD Pipelines  
✅ Used in Docker & Kubernetes  
✅ Important for Automation  
✅ Helps in Troubleshooting  

---

# 🏁 Summary

Linux commands are the foundation of DevOps and system administration.

Mastering CLI allows you to:

- Manage servers efficiently
- Automate tasks
- Troubleshoot systems
- Improve productivity

---

