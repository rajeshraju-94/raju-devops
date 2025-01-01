# below command is for checking connection between Ansible server to Ansible node
ansible -i 172.31.95.87, all -e ansible_user=ec2-user -e ansible_password="DevOps321" -m ping

172.31.95.87 = this is ansible node server private IP address
-m is the module name
