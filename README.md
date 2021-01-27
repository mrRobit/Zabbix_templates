# Zabbix template for Palo Alto Networks Next-Generation firewall

## Overview

The template to monitor Palo Alto Networks NGFW PAN-OS by Zabbix using SNMP v2c.
For Zabbix version: 5.2 and higher. It may work with older versions, but was not tested. In case of errors at older Zabbix versions please choose "Zabbix_old" branch.

This template was tested on:

- PAN-OS, version 9.1
- PAN-OS, version 10.0

## Setup

> See [Zabbix templates importing](https://www.zabbix.com/documentation/5.2/manual/xml_export_import/templates#importing) for basic instructions on how to import a template.

Create a NGFW host and link this template to it.

## Zabbix configuration

- Set/change the SNMP community in the host SNMP settings to match your community string. See [CONFIGURING SNMP MONITORING](https://www.zabbix.com/documentation/current/manual/config/items/itemtypes/snmp#configuring_snmp_monitoring)
- Set SNMP community on the NGFW and commit. See [Enable SNMP Monitoring] (https://docs.paloaltonetworks.com/pan-os/10-0/pan-os-web-interface-help/device/device-setup-operations/enable-snmp-monitoring.html)

## Template links

Linked to Template Module Interfaces SNMPv2

## Discovery rules

|Name|Description|Type|Key and additional info|
|----|-----------|----|----|
|FAN Discovery |<p>Discovery for fans</p> |SNMP agent |entPhysicalDescr[FAN]<p>**Filter**:</p><p>{#SNMPVALUE} MATCHES_REGEX `{Fan}`</p> |
|TEMPERATURE Discovery |<p>Discovery of temperature sensors</p> |SNMP agent |entPhysicalDescr[TEMPERATURE]<p>**Filter**:</p><p>{#SNMPVALUE} MATCHES_REGEX `{Temperature}`</p> |

## Items collected

|Name|Description|
|----------|--------------|
|App-ID content date |<p>Currently installed application definition release date. If no release date is found, unknown is returned.</p> |
|App-ID Version |<p>Currently installed application definition version. If no application definition is found, 0 is returned.</p> |
|Chassis type |<p>Chassis type for this Palo Alto device.</p> |
|Global Protect Client Version |<p>Currently installed global-protect client package version. If package is not installed, 0.0.0 is returned.</p> |
|GP active tunnels |<p>Number of active tunnels.</p> |
|GP gateway utilization |<p>GlobalProtect Gateway utilization percentage.</p> |
|GP tunnels supported |<p>Max tunnels allowed.</p> |
|HA Mode |<p>Current high-availability mode (disabled, active-passive, or active-active).</p> |
|HA Peer State |<p>Current peer high-availability state.</p> |
|HA State |<p>Current high-availability state.</p> |
|HW Version |<p>Hardware version of the unit.</p> |
|ICMP Check |<p>Ping to device.</p> |
|PAN-OS Version |<p>Full software version. The first two components of the full version are the major and minor versions. The third component indicates the maintenance release number.</p> |
|Processor 1 Load (mgmt) |<p>The average, over the last minute, of the percentage of time that this processor was not idle. Implementations may approximate this one minute smoothing period if necessary.</p> |
|Processor 2 Load (data) |<p>The average, over the last minute, of the percentage of time that this processor was not idle. Implementations may approximate this one minute smoothing period if necessary.</p> |
|Serial Number |<p>The serial number of the unit. If not available, an empty string is returned.</p> |
|Session table utilization |<p>Session table utilization percentage. Values should be between 0 and 100.</p> |
|SNMP availability |<p>SNMP availability.</p> |
|System Description |<p>A textual description of the entity.  This value should include the full name and version identification of the system's hardware type, software operating-system, and networking software.  It is mandatory that this only contain printable ASCII characters.</p> |
|System Name |<p>An administratively-assigned name for this managed node.  By convention, this is the node's fully-qualified domain name.</p> |
|System Uptime |<p>The time (in hundredths of a second) since the network management portion of the system was last re-initialized. Preprocessed to seconds.</p> |
|Threat Version |<p>Currently installed threat definition version. If no threat definition is found, 0 is returned.</p> |
|Total active ICMP sessions |<p>Total number of active ICMP sessions.</p> |
|Total active sessions |<p>Total number of active sessions.</p> |
|Total active TCP sessions |<p>Total number of active TCP sessions.</p> |
|Total active UDP sessions |<p>Total number of active UDP sessions.</p> |
|Total supported sessions |<p>Total number of sessions supported.</p> |
|URL Filtering Version |<p>Currently installed URL filtering version. If no URL filtering is installed, 0 is returned.</p> |

## Triggers

Appropriate triggers are associated with the items

## Feedback

Please report any issues with the template here in the "Issues" tab.
