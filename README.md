# coding-tips

### Set up a cronjob

In order to schedule a task to run on a regular basis use one of the following options:
 - Put a shell script in one of these folders: `/etc/cron.daily`, `/etc/cron.hourly`, `/etc/cron.monthly` or `/etc/cron.weekly`. Pay attention that These are system-wide and run with high privileges.
 - Open your personal crontab using `crontab -e`. The first line in that file explains everything you need to know.

### Change the OS hostname

 - The following command makes it work only until you restart: `sudo hostname your-new-hostname`.
 - After a restart your changes in `/etc/hostname` will be used, so you should replace the hostname in that file.
 - You should also edit `/etc/hosts` and change the line which reads `127.0.1.1 your-old-hostname` so that it now contains your new hostname.

