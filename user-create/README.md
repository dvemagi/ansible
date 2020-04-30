# Ansible per attivare gli utenti di amministrazione

### Primo modo di installazione
Al momento della creazione dell'istanza in advanced details editare lo user data /
attenzione ci volgiono circa 3 min affinche gli script finiscano

#### per Amazon Linux
```
#!/bin/bash
sudo amazon-linux-extras enable ansible2
sudo yum install ansible -y
sudo yum install git -y
cd /home/ec2-user
git clone https://github.com/dvemagi/ansible.git
cd ansible/user-create/
sudo ansible-playbook user-amz2.yaml
```

#### per Ubuntu
```
> #!/bin/bash
 sudo amazon-linux-extras enable ansible2
 sudo yum install ansible -y
 sudo yum install git -y
 cd /home/ec2-user
 git clone https://github.com/dvemagi/ansible.git
 cd ansible/user-create/
 sudo ansible-playbook user-ubuntu.yaml
```
### Secondo modo di installazione
Per macchine già esistenti

Installare **Ansible**
Installare  **Git**

```
 git clone https://github.com/dvemagi/ansible.git
 cd ansible/user-create/
```
A seconda se Amazon Linux o Ubuntu lanciare il comando ansible-playbook
```
ansible-playbook user-(distri).yaml
```
