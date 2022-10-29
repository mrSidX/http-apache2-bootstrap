# http-apache2-bootstrap

Sets up domain for apache2

RUN:   ```./make-site mydomain.com```


System:  Ubuntu with Apache2

This is a 2 file script and template duo that will copy the generic http settings for routing your Apache2 site.
This is a specific case for Ubuntu systems, but I'm sure further work down the line can utilize a more universal approach.

This script is geared towards my specific configuration, where I am hosting the website ```public_html``` files in the user folder:
```/home/ubuntu/www/mydomain.com/public_html/```  and symlinked to the Apache2 folders ```/var/www/mydomain.com/public_html/```


Enter your domain stated in the RUN command above.  ie  ```./make-site mydomain.com```



The script will automatically run ```certbot --apache``` to run the apache plugin.  Step should be straight forward.
I choose the redirect option, as Certbot will setup the SSL certs at the end of the script iteration.

You will need to have the certbot apache2 plugin installed.




PREREQUISITES: 
As directed from this site: https://upcloud.com/resources/tutorials/install-lets-encrypt-apache

```sudo apt-get install software-properties-common
sudo add-apt-repository universe
sudo add-apt-repository ppa:certbot/certbot
sudo apt-get update

sudo apt-get install certbot python-certbot-apache apache2
```



