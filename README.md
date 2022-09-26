# Linux Foundation Certified System Administrator (LFCS)

![](https://training.linuxfoundation.org/wp-content/uploads/2020/11/lfcs_111820-300x300.png)


## Table of Contents

- [Essential commands](#essential-commands)
  * [Log into & remote graphical and text mode consoles](#log-into-remote-graphical-and-text-mode-consoles)
  * [Read and use System Documentation](#read-and-use-system-documentation)
  * [Create, Delete, Copy and Move Files and Directories](#create-delete-copy-and-move-files-and-directories)
  * [Create and manage hard links](#create-and-manage-hard-links)
  * [Create and manage soft links](#create-and-manage-soft-links)
  * [List, set and change standard file permissions](#list-set-and-change-standard-file-permissions)
  * [SUID, SGID, and Sticky Bit](#suid-sgid-and-sticky-bit)
  * [Search for files](#search-for-files)
  * [Analyze test using basic regualar expressions](#analyze-test-using-basic-regualar-expressions)
  * [Extended Regular Expression](#extended-regular-expression)
  * [Archive, backup, compress, unpack, and uncompress files](#archive-backup-compress-unpack-and-uncompress-files)
  * [Compress and Uncompress files](#compress-and-uncompress-files)
  * [Backup files to a Remote System](#backup-files-to-a-remote-system)
  * [Use input output redirection](#use-input-output-redirection)
  
- [Operation of running systems](#operation-of-running-systems)
  * [Boot, reboot, and shutdown a system safely](#boot-reboot-and-shutdown-a-system-safely)
  * [Boot or change system nto different operating modes](#boot-or-change-system-nto-different-operating-modes)
  * [Install, configure and troubleshoot bootloaders](#install-configure-and-troubleshoot-bootloaders)
  * [Use scripting to automate system maintenance tasks](#use-scripting-to-automate-system-maintenance-tasks)
  * [Manage the startup process and service (In Services Configuration)](#manage-the-startup-process-and-service---in-services-configuration)
  * [Diagnose and manage processes](#diagnose-and-manage-processes)
  * [Locate and analyze system log files](#locate-and-analyze-system-log-files)
  * [Schedule tasks to run a set date and time](#schedule-tasks-to-run-a-set-date-and-time)
  * [Verify completion of scheduled jobs](#verify-completion-of-scheduled-jobs)
  * [Update software to provide required functionality and security](#update-software-to-provide-required-functionality-and-security)
  * [Manage Software](#manage-software)
  * [Identify the component of a Linux distribution that a file belongs to](#identify-the-component-of-a-linux-distribution-that-a-file-belongs-to)
  * [Verify the integrity and availability of resources](#verify-the-integrity-and-availability-of-resources)
  * [Change kernel runtime parameters, persistent and non-persistent](#change-kernel-runtime-parameters-persistent-and-non-persistent)
  * [List and Identify SELinux AppArmor file and process contexts](#list-and-identify-selinux-apparmor-file-and-process-contexts)
  
- [User and Group Management](#user-and-group-management)
  * [Create, delete, and modify local user accounts](#create-delete-and-modify-local-user-accounts)
  * [Create, delete, and modify local groups and group memberships](#create-delete-and-modify-local-groups-and-group-memberships)
  * [Manage system-wide enviroment profiles](#manage-system-wide-enviroment-profiles)
  * [Manage template user enviroment](#manage-template-user-enviroment)
  * [Configure user resource limits](#configure-user-resource-limits)
  * [Manage user privileges](#manage-user-privileges)
  * [Manage access to the root account](#manage-access-to-the-root-account)
  * [Configure PAM](#configure-pam)

- [Networking](#networking)
  * [Configure netowrking and hostname resolution statically or dynamically](#configure-netowrking-and-hostname-resolution-statically-or-dynamically)
  * [Configure network services to start automatically at reboot](#configure-network-services-to-start-automatically-at-reboot)
  * [Start, stop, and check the status of network services](#start-stop-and-check-the-status-of-network-services)
  * [Implement packet filtering](#implement-packet-filtering)
  * [Statically route IP traffic](#statically-route-ip-traffic)
  * [Synchronize time using other network peers](#synchronize-time-using-other-network-peers)

- [Service Configuration](#service-configuration)
  * [Configire a caching DNS server](#configire-a-caching-dns-server)
  * [Maintain a DNS zone](#maintain-a-dns-zone)
  * [Configure email aliases](#configure-email-aliases)
  * [Configure an IMAP and IMAPS service](#configure-an-imap-and-imaps-service)
  * [Configure SSH servers and clients](#configure-ssh-servers-and-clients)
  * [Restrict access to the HTTP proxy server](#restrict-access-to-the-http-proxy-server)
  * [Configure an HTTP server](#configure-an-http-server)
  * [Configure HTTP server log files](#configure-http-server-log-files)
  * [Restrict access to a web page](#restrict-access-to-a-web-page)
  * [Configure a database server](#configure-a-database-server)
  * [Manage and configure containers](#manage-and-configure-containers)
  * [Manage and configure Vertual Machines](#manage-and-configure-vertual-machines)

- [Storage Management](#storage-management)
  * [List, create, delete, and modify physical storage partitions](#list-create-delete-and-modify-physical-storage-partitions)
  * [Configure and manage swap space](#configure-and-manage-swap-space)
  * [Create and configure file systems](#create-and-configure-file-systems)
  * [Configure systems to mount file systems at or during boot](#configure-systems-to-mount-file-systems-at-or-during-boot)
  * [Evaluate and compare the basic file system feature and options](#evaluate-and-compare-the-basic-file-system-feature-and-options)
  * [Manage and configure LVM storage](#manage-and-configure-lvm-storage)
  * [Create and configure excrypted storage](#create-and-configure-excrypted-storage)
  * [Create and manage RAID devices](#create-and-manage-raid-devices)
  * [Setup user and group disk quotes for filesystems](#setup-user-and-group-disk-quotes-for-filesystems)



# Essential commands

## Log into remote graphical and text mode consoles
```console
$ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group
default qlen 1000
link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
inet 127.0.0.1/8 scope host lo
valid_lft forever preferred_lft forever
inet6 ::1/128 scope host
valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state
UP group default qlen 1000
link/ether 08:00:27:6b:d7:87 brd ff:ff:ff:ff:ff:ff
inet 192.168.0.17/24 brd 192.168.0.255 scope global dynamic
noprefixroute enp0s3
valid_lft 1966sec preferred_lft 1966sec
inet6 fe80::a00:27ff:fe6b:d787/64 scope link noprefixroute
```
```console
$ ssh user@ip
Activate the web console with: systemctl enable --now cockpit.socket
Last login: Tue Oct 19 20:27:15 2021 from 192.168.0.3
```
## Read and use System Documentation
```console
$ ls --help
$ ls -l
$ journalctl --help
$ man journalctl
$ man man
$ man 1 printf
$ man 3 printf
$ apropos directory
$ sudo mandb
$ apropos director
$ systemctl                             [TAB TAB TAB]
$ systemctl list -dependecies           [TAB]
```
## Create Delete Copy and Move Files and Directories
```console
$ ls
$ ls -a
$ ls -l /var/log/
$ ls -al
$ ls -alh
$ pwd
$ cd /var/log/
$ cd ..
4 cd /
$ cd -
$ cd
$ touch file.txt
$ touch /home/bob/file.txt
$ touch ../bob/file.txt
mkdir Files
cp file.txt Files/
cp -r Files/ BackupFiles/
mv file.txt Files/
rm files.txt
rm -r Files/
```
## Create and manage hard links
```console
```
## Create and manage soft links
```console
```
## List set and change standard file permissions
```console
```
## SUID SGID and Sticky Bit
```console
```
## Search for files
```console
```
## Analyze test using basic regualar expressions
```console
```
## Extended Regular Expression 
```console
```
## Archive backup compress unpack and uncompress files
```console
```
## Compress and Uncompress files
```console
```
## Backup files to a Remote System
```console
```
## Use input output redirection
```console
```

# Operation of running systems
## Boot reboot and shutdown a system safely
## Boot or change system nto different operating modes
## Install configure and troubleshoot bootloaders
## Use scripting to automate system maintenance tasks
## Manage the startup process and service - In Services Configuration
## Diagnose and manage processes
## Locate and analyze system log files
## Schedule tasks to run a set date and time
## Verify completion of scheduled jobs
## Update software to provide required functionality and security
## Manage Software
## Identify the component of a Linux distribution that a file belongs to 
## Verify the integrity and availability of resources
## Change kernel runtime parameters, persistent and non-persistent
## List and Identify SELinux AppArmor file and process contexts

# User and Group Management
## Create delete and modify local user accounts
## Create delete and modify local groups and group memberships 
## Manage system-wide enviroment profiles
## Manage template user enviroment 
## Configure user resource limits
## Manage user privileges
## Manage access to the root account
## Configure PAM

# Networking
## Configure netowrking and hostname resolution statically or dynamically 
## Configure network services to start automatically at reboot
## Start stop and check the status of network services 
## Implement packet filtering
## Statically route IP traffic
## Synchronize time using other network peers

# Service Configuration
## Configire a caching DNS server
## Maintain a DNS zone
## Configure email aliases
## Configure an IMAP and IMAPS service
## Configure SSH servers and clients
## Restrict access to the HTTP proxy server
## Configure an HTTP server
## Configure HTTP server log files
## Restrict access to a web page 
## Configure a database server
## Manage and configure containers 
## Manage and configure Vertual Machines

# Storage Management
## List create delete and modify physical storage partitions
## Configure and manage swap space
## Create and configure file systems
## Configure systems to mount file systems at or during boot 
## Evaluate and compare the basic file system feature and options
## Manage and configure LVM storage
## Create and configure excrypted storage 
## Create and manage RAID devices 
## Setup user and group disk quotes for filesystems



## Heading 2 link [Heading link](https://github.com/pandao/editor.md "Heading link")
## Headerdds (Underline)
