# below command is for checking connection between Ansible server to Ansible node
ansible -i 172.31.95.87, all -e ansible_user=ec2-user -e ansible_password="DevOps321" -m ping

172.31.95.87 = this is ansible node server private IP address
-m is the module name

# below command is to run any ansible play book from server to the node
ansible-playbook -i inventory.ini -e ansible_user=ec2-user -e ansible_password="DevOps321" 01-ping-pong.yaml

# below command is to pass the values from the arguments

ansible-playbook -i inventory.ini -e ansible_user=ec2-user -e ansible_password="DevOps321" -e "Name=Rajesh Greeting=Evening" 09-vars-from-args.yaml

# below command is to list "ungrouped" / "grouped" servers from inventory file
ansible -i inventory.ini ungrouped --list-hosts

ansible -i inventory.ini web --list-hosts

ansible -i inventory.ini all --list-hosts ==> to see all servers from inventory file


