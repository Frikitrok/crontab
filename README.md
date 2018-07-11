# crontab
## run from user u want to create rule
crontab -e
## rule while vm start
@reboot do_the_thing.sh

## Example of job definition:
--------------- minute (0 - 59)
  .------------- hour (0 - 23)
      .---------- day of month (1 - 31)
          .------- month (1 - 12) OR jan,feb,mar,apr ...
             .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
*  *  *  *  * user-name  command to be executed

## perform every day at 01.01 am script
01 01 * * * /usr/local/bin/try_shutdown.sh