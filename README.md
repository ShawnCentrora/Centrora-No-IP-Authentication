Centrora No-IP Authentication plugin adds an additional check for the website admin account login at both back-end and front-end. 

Restricting the IP access of the admin accounts can efficiently protect the website from the brute-force. Even the admin account has been stolen, setting the IP control can stop the hacker logging in the website to do more harms. However, it's not easy to restrict the IPs when you have a dynamic IP instead of the static IP. Centrora No-IP plugin can help in this case. You can generate a free host with No-IP and associate the host with your PC. Then you just need to whitelist the host with the plugin to grant the access to you PC only.

### Installation  

Please download the IP at [here](https://github.com/ShawnOSE/Centrora-No-IP-Authentication/archive/master.zip). Install it in Joomla! Extension --> Install. 

### Register a host with No-IP

First, go the link https://www.noip.com/sign-up to create an account. Login and go to the menu **Dynamic DNS** --> **Hostnames**. Add a new Hostname.
<img src="https://cdn.protect-website.co/centrora_web/images/Community/Centrora No-IP Authentication/2017-03-19_09-40-38.png">

Then install Dynamic Update Client on your PC. Go to the menu **Dynamic DNS** --> **Dynamic Update Client**, https://www.noip.com/download. Download and install it. You can configure it to make it start with your system. Login with your No-IP account and enable the Host in **Edit Hosts**.
<img src="https://cdn.protect-website.co/centrora_web/images/Community/Centrora No-IP Authentication/2017-03-19_09-49-54.png">

Now, your PC has been associated with the hostname.

### Configure the plugin

1. Go to Joomla! plugin manager;
2. Disable the default joomla authentication plugin "Authentication - Joomla";
3. Enable "plg_authentication_joomla_noip".
4. Configure the plugin to input the no-ip hostnames. Separate them with ',' if there are multiple hostnames.

### Test 

Now, let's see how it works. Go to the site login form (back-end or front-end) and login with the admin account from a PC without the No-IP Host associated. You will get the No Authentication error and the login is blocked.
<img src="https://cdn.protect-website.co/centrora_web/images/Community/Centrora No-IP Authentication/2017-03-19_09-59-15.png">
