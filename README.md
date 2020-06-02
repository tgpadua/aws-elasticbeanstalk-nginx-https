# AWS Elastic Beanstalk NGINX HTTPS
Sample project enabling HTTPS on Node.JS + NGINX platform

## Obtain the project
Clone the GitHub repository
```
git clone https://github.com/tgpadua/aws-elasticbeanstalk-nginx-https.git
```

## Insert your keys and certs
Edit the file **.ebextensions/https-instance.config** and update with your certificate and key in the following sections
```
      -----BEGIN CERTIFICATE-----
      certificate file contents
      -----END CERTIFICATE-----

      -----BEGIN RSA PRIVATE KEY-----
      private key contents
      -----END RSA PRIVATE KEY-----
```

## Packing
Packing the content 
```
cd aws-elasticbeanstalk-nginx-https
zip -rv ../app.zip * .ebextensions/* .platform/*
```

## Reference
https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/platforms-linux-extend.html
