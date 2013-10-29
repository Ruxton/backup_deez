Backup Deeze (tings right hur)
====================================

Overview
--------

This set of scripts is something I use to create daily backups on my systems.

It's a combination of:
* Killer BASH skills
* Cron
* Tar

Requirements
------------

A POSIX compliant system with:
* Bash (>= 4)
* Sed
* Tar
* Cron (optional, you can choose to run them however you want)
* MySQL (optional, if you want to backup MySQL DB's)

Using Backup Deeze
------------------

1. Create a new backup descriptor by running backup-create
2. Edit your user crontab `crontab -e`
3. Ensure to set $HOME to your home directory in crontab
4. Add /usr/local/bin/backupd to run whenever you want backups to run eg. `0 5 * * * /usr/local/bin/backupd`
5. Save.

Meta
----

* Code: `git clone git://github.com/ruxton/backup_deeze.git`
* Home: <http://ignite.digitalignition.net/>