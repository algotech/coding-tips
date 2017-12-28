# coding-tips

### Set up a cronjob

In order to schedule a task to run on a regular basis use one of the following options:
 - Put a shell script in one of these folders: `/etc/cron.daily`, `/etc/cron.hourly`, `/etc/cron.monthly` or `/etc/cron.weekly`. Pay attention that These are system-wide and run with high privileges.
 - Open your personal crontab using `crontab -e`. The first line in that file explains everything you need to know.
