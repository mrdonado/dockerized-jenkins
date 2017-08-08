# Instructions to start docker without iptables

Edit the file `/etc/system.d/system/docker.service.d` and type:

```
[Service]
ExecStart=
ExecStart=/usr/bin/docker daemon -H fd:// --iptables=false
```

In order to start docker, type:

`sudo systemctl docker start`

# Manage your iptables

Relevant files:

```
/etc/sysconfig/iptables
/etc/sysconfig/ip6tables
```

Restart services:

```
systemctl restart iptables
systemctl restart ip6tables
```
