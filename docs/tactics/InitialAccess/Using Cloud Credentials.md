---
hide:
  - toc
  - footer
---

# Using Cloud Credentials

!!! info inline end
    ID: ???<br>
    Tactic: [Initial Access](../InitialAccess/index.md)

In cases where the Kubernetes cluster is deployed in a public cloud (e.g., AKS in Azure, GKE in GCP, or EKS in AWS), compromised cloud credential can lead to cluster takeover. Attackers who have access to the cloud account credentials can get access to the cluster’s management layer.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|