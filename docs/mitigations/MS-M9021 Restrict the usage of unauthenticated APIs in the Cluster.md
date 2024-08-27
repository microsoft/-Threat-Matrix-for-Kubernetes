---
hide:
  - toc
  - footer
---

# Restrict the usage of unauthenticated APIs in the cluster

!!! info inline end
    ID: MS-M9021<br>
    MITRE mitigation: -


Some unmanaged clusters are misconfigured such as anonymous access is accepted by the Kubernetes API server. Make sure that the Kubernetes API is configured properly, and authentication and authorization mechanisms are set.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9024](../techniques/Connect%20from%20Proxy%20server.md)|Connect from proxy server|Restrict unauthenticated API to the Kubernetes API server.|
|[MS-TA9042](../techniques/Data%20manipulation.md)|Data manipulation|Restrict the usage of unauthenticated application APIs in the cluster.|
|[MS-TA9043](../techniques/Data%20exfiltration.md)|Data exfiltration|Restrict the usage of unauthenticated application APIs in the cluster.|