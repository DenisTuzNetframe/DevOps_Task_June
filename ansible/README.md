# The Ansible block

ansible-playbook devops_test_local_vens.yml --list-tasks
ansible-playbook devops_test_remote_vens.yml --list-tasks

ansible-playbook -l devops_test_local devops_test_local_vens.yml

ansible-inventory --list
ansible devops_test_local_vens -m ping
ansible devops_test_local_vens -m setup
ansible devops_test_local_vens -m shell -a "uptime"
ansible devops_test_local_vens -m copy "src=file dest=/ mode=777" -b
ansible devops_test_local_vens -m file -a "path=file state=absent" -b
ansible devops_test_local_vens -m get_url -a "url=https:// dest=/" -b
