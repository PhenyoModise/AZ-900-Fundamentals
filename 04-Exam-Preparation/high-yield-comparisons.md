# High-yield AZ-900 comparisons

[← Exam prep hub](README.md) · [Next: Quick revision →](quick-revision.md)

These are the kinds of choices that turn a simple definition into an exam scenario.

## Service and management models

| Pair | First option | Second option |
|:--|:--|:--|
| **IaaS vs PaaS** | IaaS: manage guest OS | PaaS: manage app/data, not guest OS |
| **PaaS vs SaaS** | PaaS: build and deploy apps | SaaS: use finished software |
| **Scaling up vs out** | Change machine size | Change instance count |
| **Reliability vs predictability** | Recover from failures | Forecast performance/cost |
| **CapEx vs OpEx** | Up-front capital purchases | Ongoing operational consumption |

## Azure infrastructure and networking

| Pair | Distinction |
|:--|:--|
| **Region vs availability zone** | Region = geographic area; zone = physically separate datacenter group within a region |
| **Availability set vs availability zone** | Set = fault/update domain distribution; zone = physical zone separation |
| **VPN Gateway vs ExpressRoute** | VPN uses encrypted tunnelling; ExpressRoute uses private provider connectivity |
| **VNet peering vs VPN** | Peering connects VNets via Azure backbone; VPN uses VPN gateways/tunnels |
| **Public vs private endpoint** | Publicly routed service endpoint vs service access through a private IP |
| **Azure DNS vs Azure Private DNS** | Public DNS zones vs internal DNS resolution for private networks |

## Storage and migration

| Pair | Distinction |
|:--|:--|
| **Blob vs Azure Files** | Object storage vs managed file shares |
| **Azure Files vs Managed Disks** | Network-accessible shares vs VM block disks |
| **LRS vs ZRS** | Replicas within one location vs across availability zones |
| **GRS vs GZRS** | Geo-replication with LRS primary vs ZRS primary |
| **Azure Migrate vs Data Box** | Workload discovery/assessment/migration vs physical bulk data transfer |
| **AzCopy vs Storage Explorer** | Command-line transfer vs GUI management |

## Identity, governance and monitoring

| Pair | Distinction |
|:--|:--|
| **Authentication vs authorisation** | Prove identity vs determine permissions |
| **Conditional Access vs RBAC** | Sign-in conditions vs resource operations allowed |
| **Entra ID vs Entra Domain Services** | Cloud identity vs managed legacy AD-compatible domain functionality |
| **Azure Policy vs RBAC** | Enforce standards vs grant access |
| **ReadOnly vs Delete lock** | Block writes/deletes vs block delete |
| **Pricing Calculator vs Cost Management** | Estimate planned costs vs analyse actual/forecast spending |
| **Advisor vs Monitor** | Improvement recommendations vs telemetry/alerts |
| **Service Health vs Resource Health** | Azure incidents affecting your deployment vs an individual resource state |
| **Azure Arc vs Azure Migrate** | Manage outside Azure vs move workloads into Azure |

> [!TIP]
> In an exam scenario, underline the requested **action**: **estimate, migrate, monitor, restrict, authenticate, replicate, deploy, or recommend**. Then map that action to the correct tool.
