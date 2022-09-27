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
  * [Compare and manipulate content](#compare-and-manipulate-content)
  * [Search file using Grep](#search-file-using-grep)
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
### Current / Working Directory
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
```
### Creating Files 
```console
$ touch file.txt
$ touch /home/bob/file.txt
$ touch ../bob/file.txt
```

### Creating Directories
```console
$ mkdir Files
```

### Moving Files and Directories
```console
$ cp file.txt Files/
$ cp -r Files/ BackupFiles/
```

### Moving Files
```console
$ mv file.txt Files/
```

### Deleting Files and Directories
```console
$ rm files.txt
$ rm -r Files/
```
## Create and manage hard links
### Inodes
```console
$ echo “Picture of Milo the dog” > Pictures/family_dog.jpg
$ stat Pictures/family_dog.jpg
File: Pictures/family_dog.jpg
Size: 49 Blocks: 8 IO Block: 4096 regular file
Device: fd00h/64768d Inode: 52946177 Links: 1
Access: (0640/-rw-r-----) Uid: ( 1000/ aaron) Gid: ( 1005/ family)
Context: unconfined_u:object_r:user_home_t:s0
Access: 2021-10-27 16:33:18.949749912 -0500
Modify: 2021-10-27 14:41:19.207278881 -0500
Change: 2021-10-27 16:33:18.851749919 -0500
Birth: 2021-10-26 13:37:17.980969655 -0500
```
### Hard Links
```console
$ cp –r /home/aaron/Pictures/ /home/jane/Pictures/
$ ln /home/aaron/Pictures/family_dog.jpg /home/jane/Pictures/family_dog.jpg
# ln path_to_target_file path_to_link_file

$ stat Pictures/family_dog.jpg
File: Pictures/family_dog.jpg
Size: 49 Blocks: 8 IO Block: 4096 regular file
Device: fd00h/64768d Inode: 52946177 Links: 2
Access: (0640/-rw-r-----) Uid: ( 1000/ aaron) Gid: ( 1005/ family)
Context: unconfined_u:object_r:user_home_t:s0
Access: 2021-10-27 16:33:18.949749912 -0500
Modify: 2021-10-27 14:41:19.207278881 -0500
Change: 2021-10-27 16:33:18.851749919 -0500
Birth: 2021-10-26 13:37:17.980969655 -0500

$ rm /home/aaron/Pictures/family_dog.jpg
$ rm /home/jane/Pictures/family_dog.jpg
```
### Limitations and Considerations
```console
$ useradd –a –G family aaron
$ useradd –a –G family jane
$ chmod 660 /home/aaron/Pictures/family_dog.jpg
```

## Create and manage soft links
```console
# ln -s path_to_target_file path_to_link_file
$ ln –s /home/aaron/Pictures/family_dog.jpg family_dog_shortcut.jpg
$ ls -l
lrwxrwxrwx. 1 aaron aaron family_dog_shortcut.jpg -> /home/aaron/Pictures..
$ readlink family_dog_shortcut.jpg
/home/aaron/Pictures/family_dog.jpg
$ echo “Test” >> fstab_shortcut
bash: fstab_shortcut: Permission denied
$ ls -l
lrwxrwxrwx. 1 aaron aaron family_dog_shortcut.jpg -> /home/aaron/Pictures..
```
## List set and change standard file permissions

### Owners and Groups
```console
$ ls -l
$ chgrp wheel picture.jpg
$ ls -l 
-rw-r-----. 1 bob wheel 49 Oct 27 14:41 picture.jpg
$ groups
$ sudo chown jane picture.jpg
$ ls -l 
-rw-r-----. 1 jane family 49 Oct 27 14:41 picture.jpg
$ sudo chown bob:family picture.jpg
$ ls -l
-rw-r-----. 1 bob family 49 Oct 27 14:41 picture.jpg
```
### File and Directory Permissions
```console
$ ls -l
-rwxrwxrwx. 1 bob family 49 Oct 27 14:41 picture.jpg
```

| File Type        | Identifier |
| ---------------- | ----------:|
| Directory        |      d     |
| Regular File     |      -     |
| Character Device |      c     |
| Link             |      l     |
| Socket File      |      s     |
| Pipe             |      p     |
| Block Device     |      b     |

owner | group | others

### Adding Permissions
```console
$ chmod u+w picture.jpg
$ chmod o-r picture.jpg
$ chmod g=r picture.jpg
$ chmod g=rw text.txt
$ chmod g= text.txt
$ chmod g-rwx text.txt
$ chmod u+rw,g=r,o= text.txt
$ chmod u=rw,g-w text.txt
$ chmod 755 text.txt
```
### Octal Permission
| Permission | Value |
| ---------- | ----- |
|     r      |   4   |
|     w      |   2   |
|     x      |   1   |

## SUID SGID and Sticky Bit
```console
```
## Search for files
```console
$ find /usr/share/ -name '*.jpg'
$ find /lib64/ -size +10M
$ find /dev/ -mmin -1
$ find /bin/ -name file1.txt
$ find -name file1.txt              # No path -> current directory
$ find -iname bob
$ find -name "f*"
```
### Modified Time
```console
$ find -mmin [minute]
$ find -mmin 5
$ find -mmin -5
$ find -mmin +5
$ find -mtime 2                     # 24-hour periods
$ find -cmin -5                     # change Minute
```
### File Size
```console
$ find -size 512k
$ find -size +512k                  # Greater than 512 kb
$ find -size -512k                  # Less than 512 kb
```
### Search Expressions
```console
$ find -name "f*"
$ find -name "f*" -size 512k        # AND operator
$ find -name "f*" -o -size 512k     # OR operator
$ find -not -name "f*"              # NOT operator
$ find \! -name "*"                 # alternate NOT operator

$ find -perm 664                    # exactly 664 permissions
$ find -perm -664                   # at least 664 permissions
$ find -perm /664                   # any of these permissions
$ find -perm u=rw,g=rw,o=r          # exectly 664 permissions
$ find -perm -u=rw,g=rw,o=r         # at least 664 permissions
$ find -perm /u=rw,g=rw,o=r         # any of these permissions

$ find \! -perm -o=r
```
## Compare and manipulate content
```bash
$ cat users.txt
$ tac users.txt
$ tail /var/log/dnf.log
$ tail -n 20 dnf.log
$ head dnf.log
```
```bash
$ sed 's/canda/canada/g' userinfo.txt
$ sed 's/canda/canada' userinfo.txt
$ sed -i 's/canda/canada' userinfo.txt

$ cut -d ' ' -f 1 userinfo.txt         # cut first cell 
$ cut -d ',' -f 3 userinfo.txt         # cut third cell separated with ,

$ uniq countries.txt                   # delete double entries

$ sort countries
$ sort countries.txt | uniq

$ diff file1 file2                                 # difference
$ diff -c file1 file2                              # context
$ diff -y file1 file2     === $ sdiff file1 file2  # side-by-side diff
```

## Search file using Grep
```batch
$ grep 'CentOS' /etc/os-release
NAME="- CentOS Stream"
PRETTY_NAME="CentOS Stream 8"
REDHAT_SUPPORT_PRODUCT_VERSION="CentOS Stream"

$ grep 'centos' /etc/os-release
ID="centos"
CPE_NAME="cpe:/o:centos:centos:8"
HOME_URL="https://centos.org/"

$ grep -i 'centos' /etc/os-release                    # not case sensitive
NAME="CentOS Stream"
ID="centos"
PRETTY_NAME="CentOS Stream 8"
CPE_NAME="cpe:/o:centos:centos:8"
HOME_URL="https://centos.org/"
REDHAT_SUPPORT_PRODUCT_VERSION="CentOS Stream"

$ sudo grep -r 'CentOS' /etc/                          # recursive
/etc/centos-release:CentOS Stream release 8
/etc/krb5.conf.d/kcm_default_ccache:# On Fedora/RHEL/CentOS, this is /etc/krb5.conf.d/
grep: /etc/grub.d: Permission denied
/etc/yum.repos.d/CentOS-Stream-AppStream.repo:# CentOS-Stream-AppStream.repo
/etc/yum.repos.d/CentOS-Stream-AppStream.repo:# close to the client. You should use this for CentOS updates unless you are
/etc/yum.repos.d/CentOS-Stream-AppStream.repo:name=CentOS Stream $releasever - AppStream
/etc/yum.repos.d/CentOS-Stream-BaseOS.repo:# CentOS-Stream-BaseOS.repo

$ sudo grep -ir 'centos' /etc/                         # ignore case
/etc/dnf/vars/contentdir:centos
/etc/rpm/macros.dist:%centos_ver 8
/etc/rpm/macros.dist:%centos 8
/etc/lvm/archive/cs_00000-1586619700.vg:creation_host = "LFCS-CentOS" # Linux LFCS-CentOS 4.18.0-338.el8.x86_64 #1 SMP
Fri Aug 27 17:32:14 UTC 2021 x86_64
/etc/lvm/archive/cs_00000-1586619700.vg: creation_host = "LFCS-CentOS"
/etc/lvm/archive/cs_00000-1586619700.vg: creation_host = "LFCS-CentOS"
/etc/lvm/backup/cs:creation_host = "LFCS-CentOS" # Linux LFCS-CentOS 4.18.0-338.el8.x86_64 #1 SMP Fri Aug 27 17:32:14 UTC
2021 x86_64
/etc/lvm/backup/cs: creation_host = "LFCS-CentOS"
/etc/lvm/backup/cs: creation_host = "LFCS-CentOS"
/etc/centos-release:CentOS Stream release 8

$ grep -vi 'centos' /etc/os-release                    # --invert-match
VERSION="8"
ID_LIKE="rhel fedora"
VERSION_ID="8"
PLATFORM_ID="platform:el8"
ANSI_COLOR="0;31"
BUG_REPORT_URL="https://bugzilla.redhat.com/"
REDHAT_SUPPORT_PRODUCT="Red Hat Enterprise Linux 8"

$ grep -wi 'red' /etc/os-release                       # words
REDHAT_SUPPORT_PRODUCT="Red Hat Enterprise Linux 8"

$ grep -oi 'centos' /etc/os-release                    # --only-matching
CentOS
centos
CentOS
centos
centos
centos
CentOS
```

## Analyze test using basic regualar expressions
```console
$ grep '^PASS' /etc/login.defs                          # line begin with PASS
$ grep -v '^#' /etc/login.defs                          # invert | not line begin with #
$ grep '7$' /etc/login.defs                             # line ends with 7

$ grep -r 'c.t' /etc/                                   # all words include c and t
cat, cut, execute, concatenated
$ grep -wr 'c.t' /etc/                                  # only the word start with c and end with t
cut, cat

$ grep '.' /etc/login.defs                              # this looks not for special chars
$ grep '\.' /etc/login.defs                             # this looks for chars

$ grep -r 'let*' /etc/                                  # match previous element 0 or more times
files, silent, problem, leftmargin, left, letter, legal
$ grep -r '/.*/' /etc/                                  # begins with / and ends with /
/usr/, /varr/cache/, /etc/
$ grep -r '0*' /etc/                                    # Match previous 1 or more times
0000000, 231043

$ grep -r '0+' /etc/
KP0+
$ grep -r '0\+' /etc/
0, 0000, 270372, 1.0
$ grep -Er '0+' /etc/
0, 0000, 270372, 1.0
````

## Extended Regular Expression
```console
$ egrep -r '0+' /etc/
0, 0000, 270372, 1.0
````
### Previous Element can Exist this many Times
```console
$ egrep -r '0{3,}' /etc/
000
$ egrep -r '10,{,3}' /etc/
1.0, 160, 1, 100000, 10
$ egrep -r '0{3}' /etc/
000
$ egrep -r '0{3,5}' /etc/                        
000, 0000, 00000
````
### Make The Previous Element Optional
```console
$ egrep -r 'disbled?' /etc/
disble, disabled, disables
```

### Match One Thing Or The Other
```console
$ egrep -r 'enabled|disbled' /etc/
disbled, enabled
$ egrep -ir 'enabled?|disbled?' /etc/
Enabled, enabled, Disabled, disabled
```

### Ranges or Sets
[a-z] [0-9] [abz954]
```console
$ egrep -r 'c[au]t' /etc/                                     
cut, cat, deprecated, execute, shortcuts, cation

$ egrep -r '/dev/.*' /etc/
/etc/smartmontools/smartd.conf:#/dev/twl0 -d 3ware,0 -a -s L/../../2/01
/etc/smartmontools/smartd.conf:#/dev/twl0 -d 3ware,1 -a -s L/../../2/03
/etc/smartmontools/smartd.conf:#/dev/hdc,0 -a -s L/../../2/01
/etc/smartmontools/smartd.conf:#/dev/hdc,1 -a -s L/../../2/03

$ egrep -r '/dev/[a-z]*' /etc/
/etc/smartmontools/smartd.conf:#/dev/twl0 -d 3ware,0 -a -s L/../../2/01
/etc/smartmontools/smartd.conf:#/dev/hdc,0 -a -s L/../../2/01
/etc/smartmontools/smartd.conf:#/dev/hdc,1 -a -s L/../../2/03

$ egrep -r '/dev/[a-z]*[0-9]' /etc/
/etc/sane.d/v4l.conf:/dev/bttv0
/etc/sane.d/v4l.conf:/dev/video0
/etc/sane.d/v4l.conf:/dev/video1

$ egrep -r '/dev/[a-z]*[0-9]?' /etc/
/etc/smartmontools/smartd.conf:#/dev/twl0 -d 3ware,0 -a -s L/../../2/01
/etc/smartmontools/smartd.conf:#/dev/hdc,0 -a -s L/../../2/01
/etc/smartmontools/smartd_warning.sh: hostname=`eval $cmd 2>/dev/null` || continue
````
### Subexpressions
```console
$ egrep -r '/dev/[a-z]*[0-9]?' /etc/
/etc/sane.d/umax.conf:/dev/usbscanner
/etc/sane.d/epjitsu.conf:#usb /dev/usb/scanner0
/etc/sane.d/umax_pp.conf:# /dev/ppi1, ...
/etc/sane.d/fujitsu.conf:#scsi /dev/sg1

$ egrep -r '/dev/([]*[0-9]?)*' /etc/
/etc/sane.d/dc240.conf:port=/dev/ttyS0
/etc/sane.d/dc240.conf:#port=/dev/ttyd1
/etc/sane.d/dc240.conf:#port=/dev/term/a
/etc/sane.d/dc240.conf:#port=/dev/tty0p0
/etc/sane.d/dc240.conf:#port=/dev/tty01
/etc/sane.d/dc25.conf:port=/dev/ttyS0

$ egrep -r -r '/dev/(([a-z]|[A-Z])*[0-9]?)*' /etc/
/etc/sane.d/dc240.conf:port=/dev/ttyS0
/etc/sane.d/dc240.conf:#port=/dev/ttyd1
/etc/sane.d/dc240.conf:#port=/dev/term/a
```
### [^]: Negated Ranges Or Sets
```console
$ egrep -r 'http[^s]' /etc/                             # NOT https
http, httpd

$ egrep -r '/[^a-z]' /etc/                              # NOT lower case letters
/X, /4, /$, /., /
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
