Ansible Playbook: postgresql-nsr-backup
=======================================

Configure Networker backups for PostgreSQL databases

Supported OS:
-------------
* RedHat
* CentOS
* OracleLinux

Requirements
------------

This playbook requires the postgresql-nsr-backup role.

`$ ansible-galaxy install -r roles/requirements.yml`

Examples
--------

    $ ansible-playbook playbook.yml --list-tasks
    $ ansible-playbook playbook.yml --list-tags

Complete Networker backups for PostgreSQL databases configuration

    $ ansible-playbook playbook.yml

Create .nsr files (backup excludes)

    $ ansible-playbook playbook.yml --tags=postgresql_nsr_backup_configure_dot_nsr_files

Create /bin/nsr_pg_backup script and root symlinks

    $ ansible-playbook playbook.yml --tags=postgresql_nsr_backup_root_scripts

Copy backup and recovery scripts

    $ ansible-playbook playbook.yml --tags=postgresql_nsr_backup_scripts

Copy HOWTO cheatsheet file

    $ ansible-playbook playbook.yml --tags=postgresql_nsr_backup_howto_cheatsheet

Set up backup related cron jobs (WAL archives emergency)

    $ ansible-playbook playbook.yml --tags=postgresql_nsr_backup_emergency_script

	
License
-------

GPLv3 - GNU General Public License v3.0

Author Information
------------------

This playbook was created in 2018 by [Krzysztof Lewandowski](mailto:Krzysztof.Lewandowski@fastmail.fm).


