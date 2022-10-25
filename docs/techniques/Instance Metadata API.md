---
hide:
  - toc
  - footer
---

# Instance Metadata API

!!! info inline end
    ID: MS-TA9033<br>
    Tactic: [Discovery](../tactics/Discovery/index.md) <br>
    MITRE technique: [T1552.005](https://attack.mitre.org/techniques/T1552/005/)

Cloud providers provide instance metadata service for retrieving information about the virtual machine, such as network configuration, disks, and SSH public keys. This service is accessible to the VMs via a non-routable IP address that can be accessed from within the VM only. Attackers who gain access to a container, may query the metadata API service for getting information about the underlying node. For example, in Azure, the following request would retrieve all the metadata information of an instance: http:///metadata/instance?api-version=2019-06-01

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9018](../mitigations/MS-M9018%20Restricting%20cloud%20metadata%20API%20access.md)|Restricting cloud metadata API access|Restrict the access of pods to IMDS|