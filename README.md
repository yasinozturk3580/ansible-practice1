# ansible-practice1
# install ansible 
yum install epel-release -y
yum install ansible -y

#  set up inventory file connect vm1 to ansible machine
vi  /etc/ansible/hosts : save vm1 ip  address in ansible machine (vm1     ansible_host=vm1 ip address )
cat  /etc/ansible/hosts
ansible  -m ping all : check it if it connected

# create files in class1
touch  yum.yml
# run this commands for playbook 
ansible-playbook  yum.yml
ansible-playbook variables.yml
ansible-playbook  debug.yml
# systemctl status httpd  
run this command check the task in vm1 .if it works









# rm -rf ( file or folder name ) : delete it



