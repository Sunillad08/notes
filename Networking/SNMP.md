# SNMP
[Back to networking page](Networking.md)
- --
## What is SNMP?
**Simple Network Management Protocol** (SNMP) is an Internet Standard protocol for collecting and organizing information about managed devices on IP networks and for modifying that information to change device behaviour. Devices that typically support SNMP include cable modems, routers, switches, servers, workstations, printers, and more.

![snmp|700](https://upload.wikimedia.org/wikipedia/commons/thumb/2/26/SNMP_communication_principles_diagram.PNG/500px-SNMP_communication_principles_diagram.PNG)
- --
## Why SNMP is used?
SNMP is widely used in network management for network monitoring. SNMP exposes management data in the form of variables on the managed systems organized in a management information base (MIB) which describe the system status and configuration. These variables can then be remotely queried (and, in some circumstances, manipulated) by managing applications.

Runs on port 161 and 162.
- --
## SNMP Header

|IP header|UDP header|version|community|PDU-type|request-id|error-status|error-index|variable bindings|
|:--|:--|:--|:--|:--|:--|:--|:--|:--|

The seven SNMP PDU types as identified by the PDU-type field are as follows:

- GetRequest
	A manager-to-agent request to retrieve the value of a variable or list of variables. Desired variables are specified in variable bindings (the value field is not used). Retrieval of the specified variable values is to be done as an atomic operation by the agent. A Response with current values is returned.
- SetRequest
	A manager-to-agent request to change the value of a variable or list of variables. Variable bindings are specified in the body of the request. Changes to all specified variables are to be made as an atomic operation by the agent. A Response with (current) new values for the variables is returned.
- GetNextRequest
	A manager-to-agent request to discover available variables and their values. Returns a Response with variable binding for the lexicographically next variable in the MIB. The entire MIB of an agent can be walked by iterative application of GetNextRequest starting at OID 0. Rows of a table can be read by specifying column OIDs in the variable bindings of the request.
- GetBulkRequest
	A manager-to-agent request for multiple iterations of GetNextRequest. An optimized version of GetNextRequest. Returns a Response with multiple variable bindings walked from the variable binding or bindings in the request. PDU specific non-repeaters and max-repetitions fields are used to control response behavior. GetBulkRequest was introduced in SNMPv2.
- Response
	Returns variable bindings and acknowledgement from agent to manager for GetRequest, SetRequest, GetNextRequest, GetBulkRequest and InformRequest. Error reporting is provided by error-status and error-index fields. Although it was used as a response to both gets and sets, this PDU was called GetResponse in SNMPv1.
- Trap
	Asynchronous notification from agent to manager. While in other SNMP communication, the manager actively requests information from the agent, these are PDUs that are sent from the agent to the manager without being explicitly requested. SNMP traps enable an agent to notify the management station of significant events by way of an unsolicited SNMP message. Trap PDUs include current sysUpTime value, an OID identifying the type of trap and optional variable bindings. Destination addressing for traps is determined in an application-specific manner typically through trap configuration variables in the MIB. The format of the trap message was changed in SNMPv2 and the - PDU was renamed SNMPv2-Trap.
- InformRequest
	Acknowledged asynchronous notification. This PDU was introduced in SNMPv2 and was originally defined as manager to manager communication. Later implementations have loosened the original definition to allow agent to manager communications. Manager-to-manager notifications were already possible in SNMPv1 using a Trap, but as SNMP commonly runs over UDP where delivery is not assured and dropped packets are not reported, delivery of a Trap was not guaranteed. InformRequest fixes this as an acknowledgement is returned on receipt.
- --
### Source
- [Youtube video](https://youtu.be/2IXP0TkwNJU)
- [Certbros YT Video](https://youtu.be/Lq7j-QipNrI)
- [Wikipedia](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol)