# Prerequisites

### Create and copy SSH key

https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2

### Install Ansible

    sudo apt-get install -y software-properties-common
    sudo apt-add-repository ppa:ansible/ansible
    sudo apt-get update
    sudo apt-get install -y --force-yes ansible

### Configure Ansible

Add or uncomment the following configuration parameters in `/etc/ansible/ansible.cfg` file.

    [privilege_escalation]
    become=True
    become_method=sudo
    become_user=root

# After clone

- Set variables in `ansible/group_vars/all` file.
- Set server ip addresses in `ansible/hosts/prod` file.
