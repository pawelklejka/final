Installation of NGINX(load balancer, cerbot, telegraf) + 2x webapp(spring boot, telegraf)+
stats server(grafana, influx) + database(mariadb or mysql, telegraf)

==================================================

pre instalation steps
---------------------

0. Ansible is installed in version ``>=2.7.0``
1. OS should be Amazon Linux 2 AMI (HVM) or Red Hat Enterprise Linux 7.5 (HVM)
2. Set up ips in servers.ini
3. Set influxdb ip(stats server ip) in telegraf_default.conf
4. Set up preferred ports, user names, user passwords etc.
5. Put apps private ips in dashboard where stays "putapp1privateiphere" and "putapp2privateiphere"

instalation
-----------

```bash
ansible-playbook -i servers.ini infrastructure.yml
```
