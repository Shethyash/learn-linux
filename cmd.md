**Links:**

- [Linux File System Structure](https://www.thegeekstuff.com/2010/09/linux-file-system-structure/)

**System:**

- `hostname`: hostname of computer
- `hostname -i`: host IP
- `uname`: PC name
- `uname -a`: kernel info
- `uptime`: up time of the system, users online, and system load
- `/etc/os-release`: information about the OS

**User:**

- `id`: show the user and groups
- `pwd`: present working directory

**Disk & Files:**

- `mount`:
  - `mount`: list all mounted
  - `/etc/fstab`: store info about mount and fetch on boot
- `ls`: lists files
- `df`:
  - `df -h`: available disk space
  - `df -T`: view with the file system
- `cp <filename> <location>`: copy files
- `touch <filename>`: create a new file
- `mv <filename> <new location>`: move files
- `rm <filename>`: delete files
- `rmdir <dir_name>`: remove directory
- `locate -i <filename>`: locate file in Linux
- `find <location> <filename>`: find files in a specific location
- `du`:
  - `du -k / | sort -nr | more`: view bigger files only
- `free`: gives info about memory
- `lsof`: list of open files
- `vmstate`
- `iostat`
- `iftop`

**Processes:**

- `yum whatprocvides netstat/nc`: find the main package name
- `systemctl --version`: check if systemd is installed on the system
- `ps`:
  - `ps -ef`
  - `ps -ef | grep system`: check if systemd is running
- `systemctl --all`: all running services
- `systemctl stop/start/restart/status service`
- `systemctl reload service`: reload configuration
- `systemctl enable/disable service`: start service at boot
- `systemctl mask|unmask service`: enable or disable service completely
- `rpm -qa`: list down all packages
- `top`: display Linux processes
- `kill`: kill the process

**SSH:**

- secured shell
- `/etc/ssh/shhd_config`: config file for SSH
- `ssh keygen`: to generate the keygen
- `ssh-copy-id root@ip`: to copy pub key to the remote server so that the remote server can access without a password

**Logs:**

- `/var/log`: main location for logs
- `boot`: booting logs
- `chronyd`: time-related logs
- `cron`: cron-related logs
- `maillog`: mail-related logs
- `secure`: SSH session logs
- `messages`
- `httpd`: some of the common log directories

**NTP:**

- `chronyd`: is the process
- `/etc/chrony.conf`: configuration file
- `timedatectl --help`: command to access many things
- `chronyc`: command-line mode for chrony

**Networking:**

- network components:
  - network interface
  - MAC address
  - subnet mask
  - gateway
  - DNS (Domain Name System)
- static IP: does not change
- DHCP (Dynamic Host Control Protocol): it changes every time it reboots
- private IP: for internal communication
- public IP: to access the internet
- network files:
  - `/etc/sysconfig/network-scripts/`: everything related to the network stored here
  - `/etc/hosts`: local DNS for the system
  - `/etc/hostname`: modify the hostname
  - `/etc/resolve.conf`: to find the DNS for your system
  - `/etc/nsswitch.conf`
- commands:
  - `nslookup www.google.com`: gives info about the gateway and end server
  - `tcpdump`:
    - all info about network coming in and going out
    - `tcpdump -i eth0`: network of eth0
  - `netstat`:
    - `netstat -rnv`: gateway info
    - `netstat -a`: all connections
    - `netstat -au/at`: all UDP or TCP networks
  - `NetworkManager`:
    - `systemctl status NetworkManager`
  - `ping`
  - `ifconfig` or `ip`
  - `traceroute`
  - `dig`
  - `ifup` or `ifdown`

**FTP:**

- `yum install vsftpd`
- `/etc/vsftpd/vsftpd.conf`: configuration files

**SCP:**

- Secure Copy Protocol
