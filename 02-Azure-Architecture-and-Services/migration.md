# Migrating workloads and data to Azure

[← Redundancy](redundancy.md) · [Next: Identity →](identity-and-access.md)

Your notes correctly identify two high-yield services: **Azure Migrate** for assessing and moving workloads and **Azure Data Box** for moving large datasets through physical devices.

| | **Azure Migrate** | **Azure Data Box** |
|:--|:--|:--|
| Main goal | Plan, assess and migrate suitable infrastructure and workloads | Transfer large data volumes when network transfer is impractical |
| Typical connection | Assessment/migration tooling, often network based | Physical device is shipped and returned |
| Best example | Move on-premises servers to Azure | Import terabytes of files where bandwidth is limited |
| Exam keyword | **Discover, assess, migrate** | **Offline bulk transfer** |

## Azure Migrate

Offers a centralised migration hub for supported workloads and partner tools. Depending on the scenario, it helps you:

1. **Discover** servers and workload dependencies.
2. **Assess** readiness, right-sizing and estimated costs.
3. **Migrate** supported servers, databases and applications using appropriate services/tools.

Your notes mention server migration, SQL assessment/migration and web app migration assistance. These are related migration workstreams, not a promise that one tool automatically migrates every system.

## Azure Data Box

Azure ships a supported physical device to an organisation. Data is copied locally to that device and the device is shipped back for ingestion into Azure.

Useful when:

- The dataset is too large for the available upload bandwidth or transfer window.
- Migration involves a major one-off bulk dataset.
- Network transfer is unreliable or expensive for the intended volume.

> [!WARNING]
> Do not memorise a universal “**80 TB maximum**.” Capacities and supported Data Box products change by model, location and service availability.

**From your notes:** Azure Migrate and Data Box workflows. **Technical correction:** device capacity is product-specific, not a timeless exam limit.
