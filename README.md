logmail
=======

logmail is a script to email errors from journald and failed units from systemd for a specified time interval.


Usage
-----

Edit the `logmail` script to fill in the parameters.

The `mailto` parameter is the email address to mail logs to and the `subject` parameter is the subject of that email.

I recommend copying the `logmail` script to your /usr/local/sbin folder and calling it from a script in one of your cron.* folders or from a systemd timer.
