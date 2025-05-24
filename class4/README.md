# create new vm for class4
# run this command for verify on class4 folder after you done with playbook.
 - ansible-playbook  -i hosts installapache.yml
# Roles 
  - Roles are packaged playbooks
  - Roles are shareable and reusable
# run this command on class4 vsc

# create an ansible role
 - install rolls on vm1 with this command : ansible-galaxy  init apache-role

# keep those folders 
 - ansible role directory structure
    - meta/         general info about your role
    - defaults/     for default variables values
    - handlers/     for handlers
    - tasks/        for playbooks
    - files/        for files to be copied to be remote machine
    - templates/    for templates.

# create ( files folder ) under apache-role folder and then install template in files folder.
- yum install wget -y
- wget   https://www.free-css.com/assets/files/free-css-templates/download/page292/grandcoffee.zip

# create ( httpd.conf.j2 ) file under template folder.
 - run this command on vm1  =  grep -v  "^#" /etc/httpd/conf/httpd.conf
 - copy, paste it in httpd.conf.j2 file.

# create setup_debian file and setup_redhat file under tasks folder.
 - install apache2 for ubuntu vm machine
 - apt install apache2 = it installs apache2 for ubuntu vm
 - systemctl status  apache2
 - ls  /etc/apache2/
 - cat /etc/apache2/apache2.conf
 - grep  -v  "^#" /etc/apache2/apache2.conf

  # Dynamic Inventory 
  # under example11 folder 
  - create aws_ec2.yml file
  # Install Python Modules  under example11 folder  
   1- curl  https://bootstrap.pypa.io/pip/2.7/get-pip.py | python
   2- pip install boto3
   3- pip install botocore
   4- pip install awscli
   1- ansible  -i  aws_ec2.yml  all -m  ping ( ansible  -i aws_ec2.yml  all  -m  ping  -u  ec2-user ) = it shows you if the all ec2 connect to ansible vm
   1.1 - export ANSIBLE_HOST_KE_CHECKING=False =(this command will disable hosts keys verification ) it skips yes, no questions.
   1.2 - and than run ping command >> ansible  -i aws_ec2.yml  all  -m  ping  -u  ec2-user 
   2- aws configure
   3- aws ec2 list
   4- aws ec2 describe-instances = its a test to have permission
   5- Make sure ec2 instances have ansible ssh key installed
   - go to ansible vm get ssh public key >>>  cat ~/.ssh/id_rsa.pub
   - go to each instance connect ec2 console run this >>> vi  ~/.ssh/id_rsa.pub copy paste ansible ssh public key
   - go to vsc and run this commands up there 1.1 and 1.2 it will be connect to all instances..
   










# cat ~/.ssh/id_rsa.pub
# cat ~/.ssh/authorized_keys
# vi  ~/.ssh/id_rsa.pub 

# To manually push your code from Visual Studio Code (VS Code) to a GitHub repository, In the VS Code terminal follow these steps:
 1- git add .
 2- git commit -m "Your commit message"
 3- git push -u origin main or master (If your branch is master then write it master instead of main.)
 OR 
 1-git add .
 2- git commit -m "Your commit message"
 3- git push

# 1-git pull
  2-git push -f origin master = ( force push )

# rm -rf ( file or folder name ) : delete it
# ansible  -i hosts  all  -m ping = check the all VM's connect.
