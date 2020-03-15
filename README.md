# Environment description

Directory "hosts" contains folders with Vagrantfiles for virtual machines.
To control (up, halt and destroy) all Vagrant VM's from "hosts" use bash-scripts:
  - vagrant_all_up.sh
  - vagrant_all_halt.sh
  - vagrant_all_destroy.sh

File "requirements.yml" contains a list of required roles.
To install roles from file use bash-script:
  - install_roles.sh
