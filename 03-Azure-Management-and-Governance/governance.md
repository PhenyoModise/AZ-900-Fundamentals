# Azure governance, compliance and resource protection

[← Cost management](cost-management.md) · [Next: Deployment →](deployment-and-management.md)

## Three commonly confused controls

| Control | What it does | Example |
|:--|:--|:--|
| **Azure Policy** | Audit or enforce resource rules | Allow only specified regions; require approved SKUs or tags |
| **Azure RBAC** | Control **who** can perform Azure resource operations | Assign Reader or Contributor at a resource group |
| **Resource lock** | Protect against accidental deletion and/or changes | Keep a critical production resource from being deleted |

### Azure Policy

Policy definitions express desired resource conditions. Assignments are applied at scopes such as **management groups**, **subscriptions** and **resource groups**. Higher-scope assignments can affect resources underneath that scope.

- **Policy definition:** one rule or evaluation.
- **Initiative:** a collection of policy definitions managed together.
- **Assignment:** applies a definition or initiative to a scope.
- **Compliance report:** shows where evaluated resources meet or violate policy rules.

> [!TIP]
> “All storage accounts must use approved regions” → **Azure Policy**. “Only certain employees may edit storage accounts” → **RBAC**.

### Resource locks

| Lock | Effect |
|:--|:--|
| **CanNotDelete / Delete** | Prevent deleting the resource, but normal permitted modifications can still occur |
| **ReadOnly** | Prevent control-plane changes as well as deletion; can interfere with operations that require write actions |

Locks inherit through supported Azure management scopes, such as a resource group's resources. Authorised administrators must remove a blocking lock before performing blocked management actions. Locks do not replace RBAC or protect every data-plane operation.

## Microsoft Purview

Microsoft Purview is a suite for **data governance, information protection, risk and compliance**. Relevant concepts in your notes include:

- Discovering and cataloguing data.
- Classifying sensitive information.
- Understanding data lineage and governance context.

Its different offerings address different governance/compliance needs; don't assume every feature is one free product.
