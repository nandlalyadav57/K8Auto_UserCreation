# k8Auto_UserCreation
 
ansible-playbook 1ec2_creation_K8Master1.yml 2ec2_creation_K8Master2.yml 3ec2_creation_K8Master3.yml 4ec2_creation_K8Worker1.yml 5ec2_creation_K8Worker2.yml 6ec2_creation_K8Worker3.yml ansible-kubeadm-contiv/site.yml --key-file "/root/K8Auto/n.pem" --extra-vars "ansible_ssh_user=ubuntu"


This will create 6EC2 instances using 6 yml files and site.yml will setup the Kubernetes cluster

Requirement on Local Machine:

yum install pip3
pip3 install boto
Local host install ansible
in you master inventory for ansible keep block for [master] [worker]  host section to register you machine

Get Below from AWS:
Keep your AWS connection Key as in code -->  
Secret Key
Access Key
Token Key /root/token/web/n.pem

k8 security group assigned with particular tcp port access 
subnetid and ami image etc. variables to be taken from aws in code