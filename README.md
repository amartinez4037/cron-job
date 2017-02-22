# cron-job

## (Logs)[http://unix.stackexchange.com/questions/207/where-are-cron-errors-logged] ##
* Check logs in /etc/rsyslog.d/50-default.conf
  * /var/log/syslog or /var/log/messages or /var/log/cron
* Email errors - /var/log/mail.err

## (Execute PHP script)[http://stackoverflow.com/questions/22358382/execute-php-script-in-cron-job] in cron job ##
* Finding the php path: whereis php
```bash
* * * * * /usr/bin/php /path/to/script.php
```

## Using cron ##

