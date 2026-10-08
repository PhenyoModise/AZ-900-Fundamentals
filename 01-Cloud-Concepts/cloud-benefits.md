# Cloud benefits, scalability and consumption pricing

[← Shared responsibility](shared-responsibility.md) · [Next: Service types →](cloud-service-types.md)

## Core cloud benefits

| Benefit | Meaning | Example |
|:--|:--|:--|
| **High availability** | Keep a service accessible despite component failures or interruptions | Deploy across availability zones where supported |
| **Scalability** | Increase or decrease capacity to match need | Add CPU/RAM or additional VMs |
| **Elasticity** | Adjust resources dynamically with demand | Autoscale a web application during traffic spikes |
| **Reliability** | Recover from failures and continue working | Use redundancy, replication and failover |
| **Predictability** | Forecast performance and spending | Monitor metrics, plan resources and estimate costs |
| **Security** | Use cloud capabilities for protection | Encryption, identity controls and threat protection |
| **Governance** | Keep resources aligned with organisational rules | Azure Policy, tags and resource locks |
| **Manageability** | Manage resources through portals, tools, templates and automation | Azure portal, CLI and PowerShell |

### Vertical vs horizontal scaling

| Scale **up/down** (vertical) | Scale **out/in** (horizontal) |
|:--|:--|
| Change the resources of **one** machine | Change the **number** of machines or instances |
| Example: upgrade a VM from 2 to 8 vCPUs | Example: increase a web app from 2 to 6 instances |
| May be limited by machine sizes | Often used with load balancing and autoscaling |

**Load balancing** distributes incoming work across suitable resources. **Autoscaling** can adjust capacity based on conditions. They often work together but are not the same thing.

## CapEx vs OpEx

| CapEx: capital expenditure | OpEx: operational expenditure |
|:--|:--|
| Up-front purchases, such as servers and a datacenter build-out | Ongoing spending on consumed services |
| Capacity often planned well in advance | Resources can usually be added or reduced more flexibly |
| Common in self-owned infrastructure | Common in pay-as-you-go cloud scenarios |

### Consumption-based model

You pay for the metered resources you use, subject to each service's pricing rules. This can reduce large up-front infrastructure purchases but **does not guarantee lower cost**. Unused billable resources, storage, data egress and poor sizing can still produce charges.

### Cloud pricing strategies

- **Pay-as-you-go:** useful for changing or uncertain demand.
- **Reserved capacity / reservations:** potentially cheaper for eligible, predictable workloads with a term commitment.
- **Savings plans:** discounts on eligible usage in exchange for a spending commitment.
- **Spot pricing:** discounted spare capacity that can be **evicted/interrupted**; suitable for fault-tolerant workloads.

> [!TIP]
> “Traffic suddenly doubles” → think **elasticity/autoscale**. “A datacenter fails but service continues” → think **reliability/high availability**. “Estimate future expenditure” → think **cost predictability**.

**From your notes:** availability, vertical/horizontal scaling, reliability, predictability, CapEx/OpEx, consumption. **Syllabus supplement:** elasticity, governance, manageability and serverless context.
