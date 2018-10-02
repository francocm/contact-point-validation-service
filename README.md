# contact-point-validation-service
A micro-service offering APIs to validate a contact point such as a mobile number, email, etc.

## Functionality

Key features:
* Feed it a contact point, and application automatically generates a unique validation reference code and sends it to the contact point.
* API to poll for contact point results.
* Callbacks to automatically notify originating application about a validation call.
* API to administer system.

Supported contact points:
* Email via SMTP
* SMS via SMPP

Physically, in terms of implementation, each contact point is abstracted, to allow for easy future expansion and support of more contact points.

## API Interfaces

The application offers two API interfaces:

| Interface | Port | Description | Swagger |
| --------- | ---- | ----------- | ------- |
| Public | 8080 | Reference code validation endpoint intended to be publicly accessible. | [link](swagger/public-api.yaml) |
| Admin | 9090 | Admin endpoint intended to be used by administrators and internal applications. | [link](swagger/admin-api.yaml) |

[TODO]

***EOF***   
