---
hide:
  - toc
  - footer
---

# Data exfiltration

!!! info inline end
    ID: MS-TA9043<br>
    Tactic: [Impact](../tactics/Impact/index.md) <br>
    MITRE technique: [T1567](https://attack.mitre.org/techniques/T1567/)

Attackers may attempt to steal sensetive application data like PII, PANs or clients credentials from linked to cluster databases, client's traffic received by pods or unrestricted inner APIs.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9014](../mitigations/MS-M9014%20Network%20Segmentation.md)|Network segmentation|Restrict inbound and outbound network traffic of the pods in the cluster.|
|[MS-M9021](../mitigations/MS-M9021%20Restrict%20the%20usage%20of%20unauthenticated%20APIs%20in%20the%20Cluster.md)|Restrict unauthenticated APIs|Restrict the usage of unauthenticated APIs in the cluster.|
