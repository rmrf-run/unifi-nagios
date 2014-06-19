**Nagios plugin to monitor status of Unifi Controller**

#Prerequisites
- working unifi install on debian
- working nagios install (tested on nagios XI on Centos)

#On Unifi box
```bash
cd
git clone https://github.com/mylivingweb/unifi-nagios.git
cp unifi-nagios/check_unifi /usr/lib/nagios/plugins
chmod +x /usr/lib/nagios/plugins/check_unifi
```
#On Nagios box
```bash
cd /usr/local/nagios/libexec/
./check_nrpe -H UNIFIIP -c check_unifi
```
