# Azure storage services, tiers and transfer tools

[← Networking](networking.md) · [Next: Redundancy →](redundancy.md)

## Core Azure Storage services

| Service | Stores | Common use |
|:--|:--|:--|
| **Azure Blob Storage** | Object/unstructured data | Images, backups, documents, logs, big data |
| **Azure Files** | Managed SMB/NFS file shares (features vary by offering) | Shared file storage for cloud and on-premises clients |
| **Azure Queue Storage** | Messages between application components | Decoupling applications |
| **Azure Table Storage** | Structured non-relational NoSQL key/attribute data | Large-scale key/value-style data |
| **Azure Managed Disks** | Block-level virtual disks | Azure VM operating system/data disks |

**Azure Data Lake Storage Gen2** adds hierarchical namespace features on Blob Storage for analytics workloads.

> [!TIP]
> “Store photos and videos” → **Blob**. “Shared file path” → **Files**. “VM disk” → **Managed Disks**. “Send messages between app parts” → **Queue**. “NoSQL key-value-style rows” → **Table**.

## Storage account basics

A storage account provides a management and naming boundary for supported Azure Storage services. Its name must meet naming rules and be unique within Azure's relevant namespace. **Public access is not automatically enabled** just because a name can be resolved.

## Blob access tiers

| Tier | Suitable data | Relative access/storage trade-off |
|:--|:--|:--|
| **Hot** | Frequently accessed | Higher storage cost, generally lower access charges |
| **Cool** | Infrequently accessed but relatively quick retrieval | Lower storage cost, usually higher access/retrieval charges |
| **Cold** | Rarely accessed, online retrieval | Lower storage cost, higher retrieval/transaction charges |
| **Archive** | Rarely accessed, long-term retention | Offline; must rehydrate before normal access |

Minimum retention periods, early deletion charges and availability differ by tier and account. Check current service documentation for exact pricing and limits.

## Moving files to and from Azure

> **Syllabus supplement:** File-transfer tools are in the official AZ-900 outline but were not substantially covered in the scanned notes.

| Tool | Primary purpose |
|:--|:--|
| **AzCopy** | Command-line copy/synchronisation to or from Azure Storage |
| **Azure Storage Explorer** | GUI tool for browsing and managing Azure Storage data |
| **Azure File Sync** | Cache/synchronise Azure Files shares with Windows Servers |
| **Azure Migrate** | Assess and move suitable on-premises workloads to Azure |
| **Azure Data Box** | Move large amounts of data by shipping a physical device |

**From your notes:** Blob, Files, Queues, Disks, Tables and Data Lake Storage Gen2. **Syllabus supplement:** storage tiers and file-transfer tools.
