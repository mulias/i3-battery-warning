i3-battery-warning
==================

This is a simple battery warning script. It uses i3's nagbar to display warnings.

Let this script run as a cronjob.

Open your crontab.

$ crontab -e

Add the folowing line to check battery status every minute

*/1 * * * * /PATH/TO/YOUR/SCRIPT/i3batwarn.sh

Added Notes
-----------
I've added a useful (if less interesting) warning message with % battery left. Also added buttons to the warning bar to Shut down, Hibernate, or Sleep the system. Each button executes the corresponding systemctl command.  

One remaining issue is that the buttons do not seem to work when the script is executed through cron. Situations I have tested:
* run script as normal user - buttons work
* run script with sudo - buttons work
* run script through user cron - buttons do not work
* run script through root cron - buttons do not work
* boot into root, run script - buttons work
* boot into root, run root cron - buttons work
Further investigation required.
 
Todo
----
* shutdown/hibernate/sleep not working with cron
