# coding-tips

### Set up a cronjob

In order to schedule a task to run on a regular basis use one of the following options:
 - Put a shell script in one of these folders: `/etc/cron.daily`, `/etc/cron.hourly`, `/etc/cron.monthly` or `/etc/cron.weekly`. Pay attention that These are system-wide and run with high privileges.
 - Open your personal crontab using `crontab -e`. The first line in that file explains everything you need to know.
 
### Create a MySQL database and a user for it from command line
 
 - Log into your MySQL database as root: `mysql -p`.
 - Create the database: `create database DATABASE_NAME;`.
 - You should then see the following appear: `Query OK, 1 row affected (0.13 sec)`.
 - Create a username and a password for your new database: `grant all privileges on DATABASE_NAME.* to 'USER_NAME'@'localhost' identified by "USER_PASSWORD";`
 - Flush the priviledges: `flush privileges;`

### Change the OS hostname

 - The following command makes it work only until you restart: `sudo hostname your-new-hostname`.
 - After a restart your changes in `/etc/hostname` will be used, so you should replace the hostname in that file.
 - You should also edit `/etc/hosts` and change the line which reads `127.0.1.1 your-old-hostname` so that it now contains your new hostname.
