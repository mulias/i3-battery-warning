i3-battery-warning
==================

This is a simple battery warning script. It uses i3's nagbar to display warnings.

Let this script run as a cronjob.

Open your crontab:
1. crontab -e
Add this line to check your battery status every minute:
2. */1 * * * * /PATH/TO/YOUR/SCRIPT/i3batwarn.sh
