# cf-espo-amazon

This script will prepare a Linux server on AWS to be used with EspoCRM and/or other web apps.
https://github.com/espocrm/espocrm

What this will do:
1. Deploy the AWS instance with a Linux system of your choice
2. Add swap, mc, htop
3. Install required dependencies to run EspoCRM (Apache, PHP (8.1), MariaDB (10.5.10), phpMyAdmin with whitelisted ip address of your choice)
4. Configure web folder, logs, etc
5. Pull an available IP address from existing ipv4 pool

Usually it takes ~8 minutes to complete. Webfolder: /web

#This script was provided AS-IS, no warranties, I would really appreciate your own commits



#How to use
1. Navigate to cloudformation
2. Select designer, copy/paste the .yml code directly
or
2. Use your S3 bucket/URL
3. Start your stack, AWS will ask you basic questions like DB username, password, favicon, etc
4. Wait for resources to deploy
5. When completed, copy public IP address, set up your DNS
6. SSH to your server, and run 'certbot' to issue a certificate

#Known todos (feel free to add)

Add backups to S3

Add EspoCRM websocket support

Add fail2ban
