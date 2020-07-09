# ar_win_iis_lecert

Ansible Role for deploying Letsencrypt certificates stored on Ansible host to IIS

By Riccardo Bicelli <r.bicelli@gmail.com>, Licensed under GNU GPL 3

## Example Playbook

```
- hosts: win_iis_servers
  become: yes
  vars:
    virtual: yes
    cert_name: my-issued-le-cert.example.com
  roles:
    - role: ar_win_iis_lecert
```

## Available variables

| Variable Name  | Explaination                        | Default Value    |
| :------------- | :----------------------------------:| ----------------:|
|  cert_name     | name of main domain of LE Cert      | Mandatory        |
|  iis_site      | IIS Web site name                   | Default Web Site |
|  http_address  | HTTP address of site is bound to    | 0.0.0.0          |
|  iis_ipaddress | Ip address on which IIS is bound to | *                |
