<div align="center">
  <h1><em>~ansible</em></h1>
</div>

This playbook installs most of the software I use on my Linux machine for software development. This is a work in project, and things will probably change as the sands of time flow.

# Project Structure
```
. ansible/
├── .ssh                      - ssh configuration files
├── auth_codes                - auth codes for various services
├── meta                      - metadata regarding this project for Ansible Galaxy
├── molecule                  - molecule tests
│   └── default
│       ├── converge.yml      - main ansible playbook
│       ├── molecule.yml      - molecule configuration
│       └── verify.yml        - molecule verification
├── tasks                     - various ansible tasks
├── README.md                 - you are here
├── ansible-run               - entry point that install ansible and runs the playbook
└── local.yml                 - ansible playbook to run locally
```

# Setup

## Running remotely

It is best to run this playbook remotely, as it is designed to be executed on a fresh install of Linux. To do so, run the following command:
```bash
bash < <(curl -s https://raw.githubusercontent.com/Kaweees/ansible/main/ansible-install)
```

Enter your account password when prompted.


##  Testing locally

Testing this playbook locally can be done by running the following command:
```bash
pip install ansible
pip install molecule[docker]
molecule init scenario -r local -d docker
molecule test
```
