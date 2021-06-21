## /etc/ansible/hosts
[ump]
ubiid ansible_host=ubiid.ubitec.local ansible_user=ops
cic ansible_host=cic-ivy.ubitec.local ansible_user=ops


## /etc/ansible/ansible.cfg to disable SSH key confirmation prompt message
host_key_checking = False

## test command
ansible all -m ping
ansible cic -a "/bin/echo hello"