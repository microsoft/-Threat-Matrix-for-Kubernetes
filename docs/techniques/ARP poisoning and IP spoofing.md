---
hide:
  - toc
  - footer
---

# ARP poisoning and IP spoofing

!!! info inline end
    ID: MS-TA9036<br>
    Tactic: [Lateral Movement](../tactics/LateralMovement/index.md) <br>
    MITRE technique: [T1557](https://attack.mitre.org/techniques/T1557/)

Kubernetes has numerous network plugins (Container Network Interfaces or CNIs) that can be used in the cluster. Kubenet is the basic, and in many cases the default, network plugin. In this configuration, a bridge is created on each node (cbr0) to which the various pods are connected using veth pairs. The fact that cross-pod traffic is through a bridge, a level-2 component, means that performing ARP poisoning in the cluster is possible. Therefore, if attackers get access to a pod in the cluster, they can perform ARP poisoning, and spoof the traffic of other pods. By using this technique, attackers can perform several attacks at the network-level which can lead to lateral movements, such as DNS spoofing or stealing cloud identities of other pods (CVE-2021-1677).

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9013](../mitigations/MS-M9013%20Restrict%20over%20permissive%20containers.md)|Restrict over permissive containers|Avoid NET_RAW capability in containers which would enable sending crafted packets that perform ARP poisoning.|
|[MS-M9028](../mitigations/MS-M9028%20Use%20CNIs%20that%20are%20not%20prone%20to%20ARP%20poisoning.md)|Use CNIs that are not prone to ARP poisoning|Use CNIs that are not prone to ARP poisoning.|