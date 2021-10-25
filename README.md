<a name="top"></a>
<div style="float:right"> 

![Thanos](./doc-img/thumb-201102.jpg)

 </div>

# wsl2-setup
How to set up a WSL development environment [Source](https://docs.microsoft.com/en-us/windows/wsl/setup/environment)




## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)

<div style="float:right"> 

[top](#top)

 </div>

## General info
A step-by-step guide to help you set up a WSL development environment using Ubuntu, Visual Studio Code, Git, and with recommended tutorials for everything you might want.

<div style="float:right"> 

[top](#top)

 </div>

## Technologies
Project is created with:
* Lorem version: 12.3
* Ipsum version: 2.33
* Ament library version: 999

<div style="float:right"> 

[top](#top)

 </div>

## Setup

### **Install WSL**
1. Open Windows Terminal Powershell tab, and type 
``` Powershell 
wsl --install
```

The --install command performs the following actions:

* Enables the optional WSL and Virtual Machine Platform components
* Downloads and installs the latest Linux kernel
* Sets WSL 2 as the default
* Downloads and installs the **_Ubuntu Linux distribution_** (reboot may be required)

### **Set up your Linux user info**

Once the process of installing your Linux distribution with WSL is complete, open the distribution (Ubuntu by default) using the Start menu. You will be asked to create a User Name and Password for your Linux distribution.

* This User Name and Password is specific to each separate Linux distribution that you install and has no bearing on your Windows user name.

* Once you create a User Name and Password, the account will be your default user for the distribution and automatically sign-in on launch.

* This account will be considered the Linux administrator, with the ability to run sudo (Super User Do) administrative commands.

* Each Linux distribution running on WSL has its own Linux user accounts and passwords. You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.


To change or reset your password, open the Linux distribution and enter the command: passwd. You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.

If you forgot the password for your Linux distribution:

1. Open PowerShell and enter the root of your default WSL distribution using the command: wsl -u root

> If you need to update the forgotten password on a distribution that is not your default, use the command: wsl -d Debian -u root, replacing Debian with the name of your targeted distribution.

2. Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: passwd <username> where <username> is the username of the account in the distribution whose password you've forgotten.

3. You will be prompted to enter a new UNIX password and then confirm that password. Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: exit.

### **Update and upgrade Linux packages**

We recommend that you regularly update and upgrade your packages using the preferred package manager for the distribution. For Ubuntu or Debian, use the command:

```bash
sudo apt update && sudo apt upgrade
```

### **Install Windows Terminal from Windows Store**
1. Go to [Windows Terminal page on Windows Store](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?rtc=1&activetab=pivot:overviewtab) and install