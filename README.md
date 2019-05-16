# Integrating The Module

To integrate the DNS Gateway Module on your cpanel or server please follow the instructions below.
Sign up on https://portal.dns.business, read and accept all the terms and condition and then request live credentials which will be sent to your email.

## On a CPANEL

login to your cpanel

### Step 1


Download the DNS Gateway Module zip here https://github.com/DomainNameServices/Gateway-WHMCS


### Note: Module names should be a single word, consisting of only lowercase letters and numbers. The name must start with a letter, and must be unique.


Now extract Gateway-WHMCS-master.zip and then rename the Gateway-WHMCS-master to dns_gateway and zip it again.


### Step 2

Now go to
```
 File Manager -> public_html -> modules -> registrars
```

### Step 4

Now upload the dns_gateway.zip on the registrar directory

### Step 5 

Reload changes



## On a Server

### Step 1 

Go to your registrars folder
```
$cd /var/www/html/modules/registrars/
```
### Step 2

Clone the module
```
sudo git clone https://github.com/DomainNameServices/Gateway-WHMCS.git
```
### Step 3

Change the module name
```
sudo mv Gateway-WHMCS/ dns_gateway
```
### Step 4

Restart apache 
```
sudo systemctl restart apache2.service
```

## Configuration

To configure WHMCS for use with DNS Gateway, follow the steps below.

1. Login to your **WHMCS admin** panel.
2. Click on **Setup** menu, select **Products/Services** and click on **Domain Registrars**.
3. Click on Activate next to DNS Gateway in the list:
![Activate Plugin](https://github.com/calebtech/pictures/blob/master/Screenshot%20from%202019-05-16%2009-09-24.png)

4. Enter your DNS Gateway API Username and API Password that you received on the email after requesting live credentials.
![Activate Plugin](https://github.com/calebtech/pictures/blob/master/Screenshot%20from%202019-05-16%2009-36-04.png)

5. Optional Settings
 - If you’re having any issues with the module it is recommended to enable DebugMode and check the logs under Utilities > Logs > Module Log. If this option is disabled the module will be logging only errors returned by the module.
 
6. Click save changes

That’s it. The DNS Gateway plug-in is now ready for use and will function just like any other built-in WHMCS registrar module. You can now make DNS Gatewayas the automatic registrar, configure TLDs and services for all your customers. To perform these actions, click on the Setup menu, select Products/Services and click on Domain Pricing in your WHMCS admin panel:

You can refer to http://docs.whmcs.com/Domains_Configuration for more information.
