# Project - Google Cloud Printer with Laravel
 
## Use Google Cloud Printer in Laravel Website

![Using Google Cloud Printer with Laravel](https://dl.dropboxusercontent.com/s/qyj4ialzkwvktu0/google-print-laravel.jpg)


Google Cloud provides many useful Products and Services :

> Google Cloud Doc
> Google Cloud Printer
> Google Cloud SQL
> Google Cloud Storage
> Google Cloud 
> etc

Here, you can see how to use Google Cloud Print in Laravel project.
###### Inegrating GoogleCloudPrint
Follw this instruction:
> You should install google cloud print package in laravel.
```php
compose require  bnbwebexpertise/laravel-google-cloud-print
```
> You should download credential.json of Google service account.
```json
{
 "type": "service_account",
 "project_id": "cloud-printer-****",
 "private_key_id": "123123123123",
 "private_key": "-----BEGIN PRIVATE KEY----- *****\n-----END PRIVATE KEY-----\n",
 "client_email": example@cloud-printer-**.iam.gserviceaccount.com",
 "client_id": "123123123123",
 "auth_uri": "https://accounts.google.com/o/oauth2/auth",
 "token_uri": "https://oauth2.googleapis.com/token",
 "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
 "client_x509_cert_url": "example.gserviceaccount.com"
  }
```
> Include json file in .env file
> Import GoogleCloudPrint class in laravel Controller or wherever you want put.
> Call print function. (Before you run asPdf(), you should create PDF file usint Laravel-Dom-PDF or something.)

```php
 GoogleCloudPrint::asPdf()
                    ->file($path.$filename.'.pdf')
                    ->printer($printerId)
                    ->send();
```

Contact us if you have problems. [link to JLCode!](https://jinlongcode.com)
