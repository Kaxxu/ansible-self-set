# ansible-self-set
Ansible playbook to configure Linux Fedora and Ubuntu workstation using the `hosts: localhost`.
If needed edit the `site.yml` file to change variables for install packages, pip, snapd.

## Playbook Usage
Install Ansible and use the command below:
```
ansible-playbook site.yml -K
```
The `-K` option will ask for the sudo password to use by Ansible.

### Terraform
In the playbook is used tag named "terraform" - It will only install terraform on the workstation. 
```
ansible-playbook site.yml -K --tags terraform

### File Structure

```
ansible-self-set
├── README.md
├── roles
│   ├── configs
│   │   ├── tasks
│   │   │   └── main.yml
│   │   └── templates
│   │       ├── ssh-config.j2
│   │       ├── terminator-config.j2
│   │       ├── tilda-autostart.j2
│   │       ├── tilda-config.j2
│   │       └── vimrc.j2
│   ├── fedora
│   │   ├── tasks
│   │   ├── main.yml
│   │   └── templates
│   │       └── docker-ce.j2
│   ├── fin
│   │   └── tasks
│   │       └── main.yml
│   ├── install
│   │   └── tasks
│   │       └── main.yml
│   └── ubuntu
│       └── tasks
│           └── main.yml
└── site.yml

13 directories, 13 files
```
