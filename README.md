# SOC Automation Lab

## Objective
Design and implement an end‑to‑end SOC automation workflow using Wazuh, TheHive, and Shuffle to streamline alert handling and accelerate response. The lab will demonstrate how Wazuh detections automatically generate cases in TheHive, trigger Shuffle playbooks to enrich events, notify analysts via automated email workflows, and execute predefined response actions. The goal is to reduce manual triage effort, improve alert fidelity, and showcase automated containment and communication capabilities within a modern SOC environment.


### Skills Learned



### Tools Used
- Wazuh
- The Hive
- Shuffle
- Oracle Virtualbox
- Windows 11
- Ubuntu
- Vultr


## Steps
1. Create diagram of automation links
<img width="1451" height="1137" alt="image" src="https://github.com/user-attachments/assets/989d81b0-182f-45d6-b259-0f97a2887719" />

2. Download and install VirtualBox, and Windows 11 iso

3. Use Vultr create both Wazuh and The Hive servers

4. Install Wazuh and The Hive using powershell

5. Configure The Hive
(nano /etc/cassandra/cassandra.yaml > change cluster name to (username) > change listen address, rpc_address, seedprovider-seed to The Hive ip address > save > systemctl stop cassandra.service > rm -rf /var/lib/cassandra/* > systemctl start cassandra.service > systemctl status cassandra.service) (nano /etc/elasticsearch/elasticsearch.yml > uncomment cluster.name, node.name, network.host, http.port, cluster.innitial_master_nodes > change cluster.name to (username) > change network.hort to The Hive ip address > remove "node-2" from cluster.innitial_master_nodes > systemctl start elasticsearch > systemctl enable elasticsearch > systemctl status elasticsearch)
6. 
