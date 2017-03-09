# cron-job
* A Linux utility which schedules a command/script on your server to run automatically at specified times/dates. Used for scheduling repetitive tasks.

## [Logs](http://unix.stackexchange.com/questions/207/where-are-cron-errors-logged) ##
* Check logs in /etc/rsyslog.d/50-default.conf
  * /var/log/syslog or /var/log/messages or /var/log/cron
* Email errors - /var/log/mail.err

## [Execute PHP script](http://stackoverflow.com/questions/22358382/execute-php-script-in-cron-job) in cron job ##
* Finding the php path: whereis php
```bash
* * * * * /usr/bin/php /path/to/script.php
```
* [Managing Cron Jobs With PHP](https://code.tutsplus.com/tutorials/managing-cron-jobs-with-php--net-19428)

## Using [crontab](http://www.computerhope.com/unix/ucrontab.htm) ##
```bash
crontab -e
```

## [Logging Output](http://www.thegeekstuff.com/2012/07/crontab-log/) ##
```bash
# Run script.sh at 5:00AM Mon-Fri and log the output to backup.log
* 5 * * 1-5 /path/to/script.sh > /path/to/backup.log 2>&1
```
* "2>&1" meaning => standard error (2>) is redirected to the same file descriptor that is pointed by standard output (&1)
* Use >> instead of > to append output
