---
hide:
  - toc
  - footer
---

# CoreDNS poisoning

!!! info inline end
    ID: MS-TA9035<br>
    Tactic: [Lateral Movement](../tactics/LateralMovement/index.md) <br>
    MITRE technique: [T1557](https://attack.mitre.org/techniques/T1557/)

CoreDNS is a modular Domain Name System (DNS) server written in Go, hosted by Cloud Native Computing Foundation (CNCF). CoreDNS is the main DNS service that is being used in Kubernetes. The configuration of CoreDNS can be modified by a file named corefile. In Kubernetes, this file is stored in a ConfigMap object, located at the kube-system namespace. If attackers have permissions to modify the ConfigMap, for example by using the container’s service account, they can change the behavior of the cluster’s DNS, poison it, and take the network identity of other services.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Limit updates permissions to the CoreDNS ConfigMap object.|