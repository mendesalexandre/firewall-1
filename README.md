GENERAL:

iptables based firewall-script with start, stop, flush and fallback functions.
To make the kernel-parameters permanent put them in the respective file(s)
(i.e. sysctl.conf) and modify them as it suits best for your application.

Additionally this project includes a small shellscript you can include in
a cronjob to get notified on extensive 'port knocking' etcetera.
The script 'contrackWarning' is self-explaining.

Just add an entry in /etc/syslog.conf (if it doesn't exist create it)
like the following:

kern.=debug     /var/log/firewall

and get notified by a 'xterm-popup' when your firewall-log grows.

Important:

Because the cronjob isn't started from a X-Session it is necessary to
export the DISPLAY (generally DISPLAY=:0) in the cron.


REQUIREMENTS:

No special requirements or dependencies.
