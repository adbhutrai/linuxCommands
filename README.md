# linuxCommands
important linux commands

# check CentOS version
  hostnamectl 
# or 
  rpm --query centos-release
# or
 cat /etc/centos-release

# No of CPU
  lscpu 
# Changing Your Password
passwd

# Add the following to /etc/sysconfig/network-scripts/ifcfg-enp0s3 (to connect internet on centos installed in virtual box on windows 10 

DNS1=8.8.8.8
DNS2=8.8.4.4
# Note this was set to no
ONBOOT=yes

# Change hostname
hostnamectl set-hostname your-new-hostname
