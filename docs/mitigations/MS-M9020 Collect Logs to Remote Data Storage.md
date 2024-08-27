---
hide:
  - toc
  - footer
---

# Collect logs to remote data storage

!!! info inline end
    ID: MS-M9020<br>
    MITRE mitigation: [M1029](https://attack.mitre.org/mitigations/M1029/)


Collect the Kubernetes and application logs of pods to external data storage to avoid tampering or deletion. This can be achieved by various open-source tools such as Fluentd. Also, built-in cloud solutions are available for managed clusters, such as Container Insights and Log Analytics in AKS and Cloud Logging in GKE.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9021](../techniques/Clear%20container%20logs.md)|Clear container logs|Collect container logs to a separate storage system.|
|[MS-TA9022](../techniques/Delete%20K8S%20events.md)|Delete Kubernetes events|Collect Kubernetes logs to a separate storage system.|
|[MS-TA9042](../techniques/Data%20manipulation.md)|Data manipulation|Collect container logs to a separate storage system.|