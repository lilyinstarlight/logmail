logmail
=======

logmail is a script to email errors from journald and failed units from systemd for a specified time interval.


Usage
-----

Edit the /etc/default/logmail file to fill in the parameters like below.

```
mailfrom="logs@example.com"
mailto="logs@example.com"
subject="Logs for $(hostname) at $(date +"%F %R")"
```

The `mailto` parameter is the email address to mail logs to and the `subject` parameter is the subject of that email.

```
$ logmail -1h err
```

I recommend copying the `logmail` script to your /usr/local/sbin folder and calling it from a script in one of your cron.\* folders or from a systemd timer.
