# ansible-playbook  -i hosts main.yml

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

# each examples folder have a .gitignore files 1-create .gitignore file and write it inside hosts before you push the folder to github repository
