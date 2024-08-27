---
hide:
  - toc
  - footer
---

# Data manipulation

!!! info inline end
    ID: MS-TA9042<br>
    Tactic: [Impact](../tactics/Impact/index.md) <br>
    MITRE technique: [T1565](https://attack.mitre.org/techniques/T1565/)

Attackers may insert, delete, or manipulate data in order to influence external outcomes or hide activity, thus threatening the integrity of the data.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9014](../mitigations/MS-M9014%20Network%20Segmentation.md)|Network segmentation|Restrict inbound and outbound network traffic of the pods in the cluster.|
|[MS-M9021](../mitigations/MS-M9021%20Restrict%20the%20usage%20of%20unauthenticated%20APIs%20in%20the%20Cluster.md)|Restrict unauthenticated APIs|Restrict the usage of unauthenticated APIs in the cluster.|
|[MS-M9020](../mitigations/MS-M9020%20Collect%20Logs%20to%20Remote%20Data%20Storage.md)|Collect Logs to Remote Data Storage|Collect container logs to a separate storage system.|