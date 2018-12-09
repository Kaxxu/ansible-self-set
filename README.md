# ansible-self-set
Ansible playbook to configure Linux Fedora and Ubuntu workstation using the `hosts: localhost`.

## Usage
Install ansible and use the commnad bellow:
```
ansible-playbook site.yml -K
```
The `-K` option will ask for the sudo password to use by ansible.

### Terraform
In the playbook is used tag named "terraform" to install terraform in the Linux. 
```
ansible-playbook site.yml -K --tags terraform
```