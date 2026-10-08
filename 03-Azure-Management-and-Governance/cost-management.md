# Azure pricing and cost management

[← Domain 3](README.md) · [Next: Governance →](governance.md)

## Factors affecting Azure cost

| Factor | Explanation |
|:--|:--|
| **Resource type, size and configuration** | Different VM sizes, disks, tiers and service settings cost different amounts |
| **Region** | Unit prices and available services can vary by geography |
| **Consumption** | Running hours, storage capacity and transactions affect charges |
| **Data transfer** | Many ingress scenarios are free; certain egress and cross-region transfers are billable |
| **Purchasing model** | Pay-as-you-go, reservations, savings plans and spot usage differ |
| **Unused resources** | Some resources remain billable even if a workload is idle or stopped in a billable state |
| **Subscriptions and offers** | Credits/discounts and eligibility can vary |
| **Azure Marketplace** | Third-party software and vendors can add licence/usage charges |

## Compare purchase models

| Model | Commitment | Best for | Caution |
|:--|:--|:--|:--|
| **Pay-as-you-go** | No long-term commitment | Variable workloads and trials | Standard on-demand unit rates |
| **Reservations** | Eligible capacity/product commitment for specified term | Predictable usage | Flexibility and cancellation/exchange terms vary |
| **Azure savings plan** | Hourly spend commitment for eligible compute over a term | Consistent compute spend across eligible services | Commitment continues during low usage |
| **Spot VMs** | No capacity guarantee | Interruptible batch/test workloads | Resources can be evicted |

> [!WARNING]
> Discount percentages in marketing or handwritten notes are **not fixed exam guarantees**. Real savings depend on service, region, term, utilisation and offer.

## Azure Pricing Calculator vs Cost Management

| Tool | When to use it |
|:--|:--|
| **Pricing Calculator** | Estimate the **potential cost** of a proposed Azure design **before deployment** |
| **Microsoft Cost Management** | Analyse and monitor **actual/forecast usage and spending**, budgets and cost allocation |
| **Budgets** | Set thresholds and alert on actual/forecast spending; not a guaranteed hard spending cap |
| **Cost analysis** | Break down costs by filters and dimensions over time |
| **Tags** | Attach metadata such as `environment=production` for organisation and cost analysis |

> [!TIP]
> **Before deployment:** Pricing Calculator. **After deployment:** Cost Management. **Warn me before overspending:** Budget alert. **Group cost by department:** Tags, resource groups and subscription design.

### Tags are metadata, not enforcement

A tag is a **key/value pair**, for example:

```text
department = engineering
environment = production
costCenter = CC-110
```

Tags help with organisation, reporting and automation. They **do not directly block deployment** or automatically propagate from resource groups to every resource; policies can help enforce tag rules.

### Three billing concepts

- **Ingress:** data transferred *into* Azure, often free for standard scenarios (exceptions exist).
- **Egress:** data transferred *out* of Azure; applicable fees may apply.
- **Billing zones:** geographic groupings used for some transfer pricing calculations, not the same as availability zones.

**From your notes:** cost factors, pricing choices, billing zones, data transfer, calculator, cost analysis, budgets and tags. **Correction:** budgets normally notify but do not automatically stop spending.
