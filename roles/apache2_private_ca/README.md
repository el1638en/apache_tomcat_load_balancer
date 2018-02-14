apache_2_private_ca
=========

Create a private certificat authority for Apache server.

Requirements
------------

OpenSSL.

Role Variables
--------------

| Name	        | Default Value	| Description|
| ------------- |:-------------:| ----------:|
|apache_2_private_ca_user|root|Owner of the Apache's directories|
|apache_2_private_ca_user_group|sys|Owner's group|
|apache_2_private_ca_md|sha256||
|apache_2_private_ca_dir|/etc/pki/apache/private_ca|Directory of private authority|
|apache_2_private_ca_key|/etc/pki/apache/private_ca/ca_key.pem|Private key of authority|
|apache_2_private_ca_cert|/etc/pki/apache/private_ca/ca_cert.pem|Public certifcat of authority|
|apache_2_private_ca_bits|2048|certifcat file is generated on 2048 bits|
|apache_2_private_ca_default_days|3650 days (10 years)|Days of expiration|
|apache_2_private_ca_country|FR|Country of code certificat authority|
|apache_2_private_ca_state|Rhone|State of certificat authority|
|apache_2_private_ca_locality|Lyon|Locality of certificat authority|
|apache_2_private_ca_organisation|Syscom|Organisation of certificat authority|
|apache_2_private_ca_organisation_unit|IT|Organisation unit of certificat authority|
|apache_2_private_ca_name|Authority Company Inc|Name of certificat authority|
|apache_2_private_ca_subj|-|All informations of certificat authority|

Dependencies
------------

None.

Example Playbook
----------------

Install apache_2_conf
```yaml
- hosts: all
  roles:
    - { role: apache_2_private_ca }
```

License
-------

BSD

Author Information
------------------
Eric LEGBA.