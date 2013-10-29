Backup Deeze (tings right hur)
====================================

![](http://puu.sh/52xnY.png)

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
4. Add /usr/local/bin/backupd to run whenever you want backups to run
5. Save.

```shell
# Runs backupd at 5am everymorning for username
HOME=/home/username
0 5 * * * /usr/local/bin/backupd
```

Transporting Backups
------------------

Backups are useless if you just leave them on the same server.  Prior to the release of BTSync I had another script in the collection that used lftp to ftp the backups to multiple locations.

These days I've installed BTSync at each of these locations, pointed it at my user back directory and the backups are automatically synced using BTSync.  Multiple users/folders allows me to sync each user individually and provide other users with a BTSync key for their own folder that they can sync themselves.

Meta
----

* Code: `git clone git://github.com/ruxton/backup_deeze.git`
* Home: <http://ignite.digitalignition.net/>