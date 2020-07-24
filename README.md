# Zabbix templates

zbx_3.0 templates are tested with Zabbix 3.0

zbx_3.4 template is edited to use with Zabbix 3.4

ZBX_4.4 template is edited to use with Zabbix 4.4:
- LLD discovery of Fans and temperature sensors
- Many direct item checks
- linked with built-in template: Template Module Interfaces SNMPv2

Note: Where a {$SNMP_PORT} macro is used in the template, please add it in the global macros (Administration -> General -> Macros). A default value is 161
