# What is this?

This Git repository explains how to notify Slack when data is submitted to Perforce.

# Howto setup
※ How to configure Slack's “Incoming Webhook” is not explained here  

Run “p4 triggers” in the server to set triggers

> example:  
> slack.notify change-commit //test-Depot/mainline/... "/opt/perforce/servers/submit-notify.sh -u %user% -c %change% -e .env"

# Edit the file named .env

PS: Password for perforce admin user  
USER: id for perforce admin user  

# About submit-notify.sh options

-u: Submitted user ID  
-c: Submitted changelist number  
-e: Config file. source command registers it in an environment variable.  
