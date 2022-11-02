##
- hosts.ini vs hosts.yml

```
[atlanta]
host1
host2

[atlanta:vars]
ntp_server=ntp.atlanta.example.com
proxy=proxy.atlanta.example.com
```
vs

```
atlanta:
  hosts:
    host1:
    host2:
  vars:
    ntp_server: ntp.atlanta.example.com
    proxy: proxy.atlanta.example.com
```



##
-  Перенос переменных в group_vars

Create new groups

```
[STAGING_NEW:children]
alias1
alias2

[STAGING_NEW::vars]


```
Crate new directory
`mkdir group_vars`
or
`mkdir host_vars`

`vim group_vars/ALIAS.yml` - for alias

`vim groups/all.yml` - for all




## Create playbook

- Install Apache and upload Web Page


- Debug, set_fact, register
 -m setup


- When block

- Jinja 
template: src = {{}} like copy

