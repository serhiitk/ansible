# Ansible
## Tasks:

- to **All** hosts:

  1) install roles - git, ntp, users, logrotate
  2) set custom NTP server:

         - "time.windows.com"
         - 10.0.0.1

  3) create users to access with ssh keys:

         labsudo
         lab
       _labsudo_  must have sudo privileges
   
  4) configure logrotate for system log `/var/log/syslog` and Apache logs `/var/log/apache2/access.log`, `/var/log/apache2/error.log`

- to **frontend** host:

  5) install **nginx** 

- to **backend** host:

  6) install **php-fpm**

## Environment description

Directory `./hosts/` contains folders with Vagrantfiles for virtual machines `vm1, ..., vm4`.
To control (_up_, _halt_ and _destroy_) all Vagrant VMs from `./hosts/` use bash-scripts:

     $ bash vagrant_all_up.sh
     $ bash vagrant_all_halt.sh
     $ bash vagrant_all_destroy.sh

File `./requirements.yml` contains a list of required Roles.
To install Roles from list use bash-script:

     $ bash install_roles.sh

## Variables

Set Roles variables for **All** hosts in `./group_vars/all.yml`

## Ansible playbook

Start Ansible playbook:

      $ ansible-playbook playbook.yml

