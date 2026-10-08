# The shared responsibility model

[← Cloud computing](cloud-computing.md) · [Next: Cloud benefits →](cloud-benefits.md)

The **cloud provider** and **customer** share responsibility for securing and operating cloud solutions. As the service becomes more managed, more underlying work shifts to the provider.

| Responsibility | On-premises | IaaS | PaaS | SaaS |
|:--|:--:|:--:|:--:|:--:|
| Physical datacenter and physical security | Customer | Provider | Provider | Provider |
| Physical servers and host networking | Customer | Provider | Provider | Provider |
| Guest operating system (where applicable) | Customer | **Customer** | Provider | Provider |
| Runtime and platform maintenance | Customer | **Customer** | Provider | Provider |
| Applications you deploy | Customer | **Customer** | **Customer** | Provider for service software |
| Data, identities and access configuration | Customer | **Shared/customer** | **Shared/customer** | **Shared/customer** |

*The table is a conceptual guide; specific tasks vary by service and configuration.*

## Responsibilities that remain yours

Even when using SaaS, customers must still make appropriate decisions about **their data, user access, account protection, configuration and compliance obligations**. The cloud provider does not magically make poor permissions safe.

## Example: Azure Virtual Machine

A virtual machine is **IaaS**:

- Microsoft runs the physical datacenter, physical hosts and underlying cloud infrastructure.
- The customer selects the VM size, manages its guest OS and patches it, deploys software, protects accounts and data, and configures access and network controls.
