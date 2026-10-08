# Azure security principles and protection

[← Identity](identity-and-access.md) · [← Domain 2](README.md) · [Continue to Domain 3 →](../03-Azure-Management-and-Governance/README.md)

## Zero Trust

Zero Trust assumes that access attempts need validation, **even from inside the organisation's network**. Its three principles are:

1. **Verify explicitly:** evaluate identity, device, context and risk.
2. **Use least privilege:** grant only the permissions needed.
3. **Assume breach:** design for containment, monitoring and recovery.

## Defense in depth

Use multiple layers of security rather than depending on a single defence.

| Layer | Typical purpose |
|:--|:--|
| **Physical security** | Protect datacenters and equipment |
| **Identity and access** | Ensure only appropriate identities can access resources |
| **Perimeter** | Guard network entry/exit points |
| **Network** | Segment, filter and inspect network traffic |
| **Compute** | Secure OS, devices and workloads |
| **Application** | Protect application logic, code and dependencies |
| **Data** | Restrict access, encrypt, back up and protect information |

## Encryption

| Type | What it protects | Example |
|:--|:--|:--|
| **At rest** | Stored data | Encrypted Azure Storage data |
| **In transit** | Data moving between systems | TLS for HTTPS traffic |

### Azure Key Vault

A managed service used to protect and manage **secrets** (such as connection strings), **cryptographic keys**, and **certificates**. It is not a replacement for all access control, network protection or secret-handling practices.

## Microsoft Defender for Cloud

> **Syllabus supplement:** Defender for Cloud is an explicitly listed AZ-900 objective, although it is not described in depth in the supplied scans.

Microsoft Defender for Cloud provides cloud security posture management and, with applicable plans, workload protection capabilities. It helps identify security recommendations and risks across supported environments.

**Compare the tools:**

| Tool | Main focus |
|:--|:--|
| **Microsoft Defender for Cloud** | Cloud security posture and workload protection |
| **Azure RBAC** | Permissions to Azure resources |
| **Conditional Access** | Identity-based access decisions |
| **Azure Key Vault** | Secret, key and certificate protection |
| **Azure Policy** | Audit/enforce resource compliance requirements |

> [!TIP]
> “Which service provides security recommendations for cloud workloads?” → **Defender for Cloud**. “Where should an app store a database credential securely?” → **Key Vault**.

**From your notes:** Zero Trust, defense in depth, encryption and Key Vault. **Syllabus supplement:** Defender for Cloud.
