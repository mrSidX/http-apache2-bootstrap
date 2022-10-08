# http-apache2-bootstrap

Sets up domain for apache2

RUN:   ```./make-site yoursite.com```


System:  Ubuntu with Apache2

This is a script I made to setup an apache2 http endpoint, given the domain name as a parameter,
this script will clear any apache2 configs of the domain if they exist, and proceed to hoist a generic
http beginner config file for the site, and setup the folders needed, ready to take the site content.

My config setups up my sites on the user end:   ~/www/domain.com/public_html
and symlinks that withing /var/www/domain.com/public_html

You can change this...

The script will automatically run 'certbot'.

You will need to have the certbot apache2 plugin installed.




PREREQUISITES: 
As directed from this site: https://upcloud.com/resources/tutorials/install-lets-encrypt-apache

```sudo apt-get install software-properties-common
sudo add-apt-repository universe
sudo add-apt-repository ppa:certbot/certbot
sudo apt-get update

sudo apt-get install certbot python-certbot-apache apache2
```



