---
title: Lab Document
date: 2019-Aug-03 23:03:10
---

- [Updated at  2018.12.19](https://docs.f5net.com/display/~jlin/F5+China+SE+Lab+Page)
- [Definition](https://docs.f5net.com/display/~jlin/F5+China+SE+Lab+Page#F5ChinaSELabPage-Definition)
- [Requirement](https://docs.f5net.com/display/~jlin/F5+China+SE+Lab+Page#F5ChinaSELabPage-Requirement)
- [DHCP Server:](https://docs.f5net.com/display/~jlin/F5+China+SE+Lab+Page#F5ChinaSELabPage-DHCPServer:)
- [Topology](https://docs.f5net.com/display/~jlin/F5+China+SE+Lab+Page#F5ChinaSELabPage-Topology)
- [Credential](https://docs.f5net.com/display/~jlin/F5+China+SE+Lab+Page#F5ChinaSELabPage-Credential)
- [Demo list (Draft)](https://docs.f5net.com/display/~jlin/F5+China+SE+Lab+Page#F5ChinaSELabPage-Demolist(Draft))
- Static IP occupation

**Note: ip bigger than 200 is reservered for static setting**

| IP addr       | Used for             | Belong to           | Owner        |
|:------------- |:---------------------|:------------------- |-------------:|
| 172.16.10.201 | K8s cluster master   | Common\_vm\_network | Jing
| 172.16.10.202 | K8s cluster node1    | Common\_vm\_network | Jing
| 172.16.10.203 | Common Demo BIGIP V13_1   | Common\_vm\_network | Jing
| 172.16.10.204 | Common Demo BIGIP V13_2   | Common\_vm\_network | Jing
| 172.16.20.208 | Common NGINX Controller   | VE\_MGMT\_network | Jing
| 172.16.10.205 | Common NGINX Controller   | Common\_vm\_network | Jing
| 172.16.20.201 | Common Demo BIGIP V12| VE\_MGMT\_network   | Jing

| IP addr       | Used for             | Belong to           | Owner        |
|:------------- |:---------------------|:------------------- |-------------:|
| 172.16.20.202 | Common Demo BIGIP V13_1| VE\_MGMT\_network   | Jing
| 172.16.30.202 | Common Demo BIGIP V13_1| VE\_external\_network   | Jing
| 172.16.40.202 | Common Demo BIGIP V13_1| VE\_internal\_network   | Jing
| 172.16.20.203 | Common Demo BIGIP V13_2| VE\_MGMT\_network   | Jing
| 172.16.30.203 | Common Demo BIGIP V13_2| VE\_external\_network   | Jing
| 172.16.40.203 | Common Demo BIGIP V13_2| VE\_internal\_network   | Jing



- Topology(Public)
<img src="/2018/09/17/Lab-Topology-0/topology-public.png">

- Definition

1. Everyone should help to maintain the lab and make sure the lab running well.
2. All pre configurations of below should not be changed or deleted.
3. Pls contact if you need change or add new perpetual F5/SW/ESXi configurations.
4. Pls clean your configurations after you completing the test.

- Requirement

1. All  perpetual common services **MUST** start with Common prefix for all  VEs/VMs/Components. The VM/VE formats in Vcenter should be: Common_function-name_system-name_version-number, for example: Common_Ansible_Centos_7.4.     
   Common named port-group in vcenter/esxi is dhcp enabled.
2. The name of  VEs/VMs/Components for personal test or temporary test **MUST** start with *your-personal-name, like linjing_mytest. And pls delete/release them immediately for other SEs once you finish your test.*
3. F5 VE **MUST** use dedicate port-groups that had defined in vcenter/esxi, all port-groups for VE have DHCP enabled.
4. Any your personal files or temp files, PLS PUT IT IN YOUR OWN FOLDER, DO NOT DROP THEM ON THE DESKTOP. 
5. If you set static IP for non-personal VLAN (in other words, means you use static ip for below DHCP subnet), **Pls change this post to include your IP**.  Otherwise VMs can be DELETED by anyone. The post content should include: which IPs and which VM/VE are using. Start time and End time.
6. Everyone can add other requirement at here, feel free to add.
