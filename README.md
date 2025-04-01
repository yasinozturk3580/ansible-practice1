# ansible-practice1
# install ansible 
1-yum install epel-release -y
2-yum install ansible -y

#  set up inventory file connect vm1 to ansible machine
1-vi  /etc/ansible/hosts : save vm1 ip  address in ansible machine     (vm1     ansible_host=vm1 ip address )
2-cat  /etc/ansible/hosts
3-ansible  -m ping all : check it if it connected

# create files in class1
touch  yum.yml
# run this command for playbook 
ansible-playbook  yum.yml
# systemctl status httpd  
run this command check the task in vm1 .if it works









# rm -rf ( file or folder name ) : delete it



