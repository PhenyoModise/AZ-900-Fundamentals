# Managing and deploying Azure resources

[← Governance](governance.md) · [Next: Monitoring →](monitoring.md)

## Tools for interacting with Azure

| Tool | Interface | Typical use |
|:--|:--|:--|
| **Azure portal** | Browser-based graphical UI | Create, view, configure and monitor services |
| **Azure Cloud Shell** | Browser-hosted shell with CLI/PowerShell options | Run commands without installing a local shell |
| **Azure CLI** | Cross-platform command-line tool | Manage Azure with `az` commands and scripts |
| **Azure PowerShell** | PowerShell cmdlets/modules | Manage Azure with objects and PowerShell automation |
| **Copilot in Azure** | AI-assisted interface | Help understand services/configuration and draft operational steps, subject to access and supported capabilities |

### Example CLI (illustrative)

```bash
# Show subscriptions visible to your signed-in identity
az account list --output table

# List resource groups in the selected subscription
az group list --output table
```

### Azure Resource Manager (ARM)

> **Syllabus supplement:** ARM, IaC and templates are current exam objectives not described in depth in the original scanned notes.

**Azure Resource Manager (ARM)** is Azure's management and deployment layer. It receives management requests and coordinates resource operations under Azure access control and governance rules.

**Infrastructure as code (IaC)** means defining infrastructure declaratively in files so it can be deployed and managed consistently. Relevant options include **ARM JSON templates** and **Bicep**.

| ARM / IaC concept | Meaning |
|:--|:--|
| **ARM template** | Declarative JSON description of resources and configuration |
| **Bicep** | A more concise Azure-focused declarative language that compiles to ARM templates |
| **Repeatable deployment** | Define and redeploy infrastructure from version-controlled configuration |
| **Resource manager** | The Azure control plane for resource management operations |

## Azure Arc for hybrid environments

Azure Arc provides Azure-style management, governance and visibility for supported resources in **on-premises and other cloud environments**. It differs from **Azure Migrate**, whose aim is moving workloads to Azure.

| Need | Consider |
|:--|:--|
| Manage local servers using Azure controls | **Azure Arc** |
| Move an existing server to Azure | **Azure Migrate** |
| Deploy infrastructure consistently from code | **ARM/Bicep** |
| Perform a quick manual configuration | **Azure portal** |
| Script resource operations | **Azure CLI / PowerShell** |
