# Integrating The Module

## On a CPANEL

To integrate the DNS Gateway Module on your cpanel please follow the instructions below.
Sign up on https://portal.dns.business, read and accept all the terms and condition and then request credentials which will be sent to your email.

Download the DNS Gateway Module zip

login to your cpanel

### Step 1

### Note: Module names should be a single word, consisting of only lowercase letters and numbers. The name must start with a letter, and must be unique.


Now extract Gateway-WHMCS-master.zip and then rename the Gateway-WHMCS-master > dns_gateway and zip it again.


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

Activate the module , and put your DNS Gateway API Username and API Password that you received on the email after requesting live credentials.
