# The Ansible block

## How to start localy:

- 0. Add your requirements.txt to './roles/files'
- 1. Run 'ansible-playbook devops_test_local_vens.yml' from './ansible'

> The './devops_test_local_vens.yml' is used for local tests.

## How to run Ansible for remote host:

- 0. Add your requirements.txt to './roles/files'
- 1. Need to add your host to './inventory/hosts.yml'
  -  Add variables to './inventory/group_vars/<example>'
- 2. Add your 'SSH key' to './ssh_key/<example_ssh_key>'
- 3. Add your Playbook config to './'
  -  Example in './devops_test_remote_vens.yml'
- 4. Run 'ansible-playbook <example>.yml' from './ansible'

================================================================================
## Ansible Map
================================================================================
'
./ansible/
|
├── ansible.cfg
├── devops_test_local_vens.yml
├── devops_test_remote_vens.yml
|
├── inventory
│   ├── group_vars
│   │   ├── devops_test_local.yml
│   │   └── devops_test_remote.yml
│   └── hosts.yml
|
├── roles
│   └── vens_test
│       ├── files
│       │   ├── test2.txt
|       |   |
│       │   └── test.txt
│       ├── tasks
│       │   └── main.yml
│       └── vars
│           └── main.yml
└── ssh_key
    └── id_rsa
'
================================================================================
================================================================================
