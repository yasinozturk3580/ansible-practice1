#  install Git in ansible vm machine = git is a version control tool,SCM source code management.
 1-yum install git  -y 
 2-git version : check if it installed

# install ansible 
 1-yum install epel-release -y
 2-yum install ansible -y

#  set up inventory file connect vm1 to ansible machine
  1-vi  /etc/ansible/hosts : save vm1 ip  address in ansible machine     (vm1     ansible_host=vm1 ip address )
  2-cat  /etc/ansible/hosts
  3-ansible  -m ping all : check it if it connected

#  create files in class1
 1.touch  yum.yml
 2.touch variables.yml
 3.touch debug.yml

#  run this command for playbook 
 1.ansible-playbook  yum.yml
 2.ansible-playbook  variables.yml
 3.ansible-playbook  debug.yml

#  systemctl status httpd  
 run this command check the task in vm1 .if it works

 #  ansible variables :variables are used to make you playbooks reusable
 #  variable.yml
 
   - hosts: web
     vars:
       package_name: "httpd"
     tasks:
     - yum:
         name: "{{ package_name }}"
         state: latest

    example (insatall apache)
      ansible-playbook variables.yml

    example (install git)
      ansible-playbook -e "package_name=git"  variables.yml
 









# rm -rf ( file or folder name ) : delete it
