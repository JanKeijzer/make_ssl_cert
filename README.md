# Windows script for creating self-signed SSL certificates

# Description

This Windows batch script creates a self-signed SSL certificate for a user defined domain. The default setting is to create a certificate that is valid for 10 years.

# Usage:

* Modify the cert-template.conf file to reflect you own information. Leave the parts with {{DOMAIN}} as is. They will be replaced by the domain names in the batch script.
* `make-cert <domain_name>`
  * This will create a subfolder named domain_name that contains two files:
    * server.key -  The private key
    * server.crt - The SSL certificate

## Remarks:

* If you want to create a wild-card domain SSL certificate use a domain_name that starts with star. Note that a wild-card domain needs at least a TLD and a second-level domain to be seen as a valid domain by Chrome.
  * Example: `make-cert star.example.com` will create a self-signed certificate for the wild-card domain: *.example.com in the subfolder star.example.com
* See [[How to Create Valid SSL in localhost for XAMPP](https://shellcreeper.com/how-to-create-valid-ssl-in-localhost-for-xampp/)](https://shellcreeper.com/how-to-create-valid-ssl-in-localhost-for-xampp/) to get instructions of how to use the certificates for development purposes.

## Links:

[How to Create Valid SSL in localhost for XAMPP](https://shellcreeper.com/how-to-create-valid-ssl-in-localhost-for-xampp/)

[GIST of Adrian Suter for modified batch file](https://gist.github.com/adriansuter/f197dac4cf8570c2214642fa15299c33)








