Zabbix-agent Role 
=================

Install Zabbix agent in active mode. This role has been specifically developed to integrate resources in the monitoring system of the INDIGO project.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.

	# Zabbix server to connect to
	zabbix_agent_server: localhost
	# Zabbix port in the server to connect to
	zabbix_agent_server_port: 10051
	# HostMetadata value in the agent config
	zabbix_agent_metadata: system.uname
	# Prefix to be added to the Hostname value in the agent config
	zabbix_agent_hostname_prefix: ""


Example Playbook
----------------

This an example of how to install the zabbix agent in active mode to the server "server.com":

    - hosts: servers
      roles:
         - { role: indigo-dc.zabbix-agent, zabbix_agent_server: server.com }

License
-------

Apache Licence v2 [1]

[1] http://www.apache.org/licenses/LICENSE-2.0
