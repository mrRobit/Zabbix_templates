# Zabbix templates

zbx_3.0 templates are tested with Zabbix 3.0<br/>
zbx_3.4 template is edited to use with Zabbix 3.4<br/>
ZBX_4.4 template is edited to use with Zabbix 4.4<br/>

# What is included in the template:
- LLD discovery of Fans
- LLD discovery of temperature sensors
- Management plane CPU
- Data plane CPU
- HA state checks
- System checks
- Security subs database versions
- Sessions checks
- many other items and triggers...

- linked with built-in template: Template Module Interfaces SNMPv2

Note: Where a {$SNMP_PORT} macro is used in the template, please add it in the global macros (Administration -> General -> Macros). A default value is 161
