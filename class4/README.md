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
