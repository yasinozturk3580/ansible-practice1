# ansible-playbook  -i hosts main.yml

# create 2 vms for example6 folder 1 is centos 1 is ubuntu 

# Example6 folder has a hosts file.
 # hosts
     [centos]
      centos1   ansible_host=

     [ubuntu]
      ubuntu1   ansible_host=

# create 1 vm for example7 folder
# Registering Variables = updating variables while running playbook.

# Example7 folder has a hosts file.(use register variables) 
 # hosts 
   [centos]
   vm1  ansible_host=

# Example8 folder has a hosts file. (use handlers)
# Handlers = Handlers are tasks which can be executed multiple times.
 # hosts 
   [centos]
   vm1  ansible_host=

 # use these commands for example8 folder on vm1 
 1- ls   /etc/httpd/conf.d/
 2- ls   /etc/httpd/conf/httpd.conf
 3- vi  /etc/httpd/conf/httpd.conf
 4- grep  ServerName      /etc/httpd/conf/httpd.conf
 5- egrep "^#ServerName"  /etc/httpd/conf/httpd.conf

 # Example9 (use NTP(network time protocol) servers 
  - ntpd ( not installed )
  - chronyd ( installed )
  
 
 1-systemctl status chronyd
 2-cat  /etc/chrony.conf
 3-cat /var/log/secure
 4- head /etc/chrony.conf



# ansible  -i hosts  all  -m ping = check the all VM's connect.

# uname  -r = it shows you the version of the Linux kernel currently running on your system.

# list of common and useful uname options, each showing a different piece of system information:
-a	       All information	                          Linux myhost 5.15.0... x86_64
-s	       Kernel name	                              Linux
-n	       Network node hostname	                    myhost
-r	       Kernel release	                            5.15.0-1051-azure
-v	       Kernel version	                            #59-Ubuntu SMP Tue Mar 19 ...
-m	       Machine hardware name (architecture)	      x86_64
-p	       Processor type                           	x86_64 or unknown
-i	       Hardware platform	                        x86_64 or unknown
-o	       Operating system	                          GNU/Linux

# each example folder has a .gitignore files 1-create .gitignore file and write it inside hosts before you push the folder to github repository


