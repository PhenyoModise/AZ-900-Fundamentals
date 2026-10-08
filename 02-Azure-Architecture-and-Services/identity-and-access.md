# Azure identity, authentication and access

[← Migration](migration.md) · [Next: Security principles →](security.md)

## Authentication vs authorisation

- **Authentication:** verify **who** someone or something is.
- **Authorisation:** decide **what** that identity is allowed to access or do.

| Service or feature | Primary role | Exam clue |
|:--|:--|:--|
| **Microsoft Entra ID** (formerly Azure AD) | Cloud identity and access management | Sign-ins, user/group identities, SSO |
| **Microsoft Entra Connect Sync** | Synchronise supported identity information from on-premises AD to Entra ID | Hybrid identities |
| **Microsoft Entra Domain Services** | Managed AD-compatible domain services for legacy apps | Domain join, LDAP, Kerberos/NTLM, Group Policy without customer-operated domain controllers |
| **Single sign-on (SSO)** | Authenticate once to access multiple integrated apps | Fewer repeat logins |
| **Multifactor authentication (MFA)** | Require more than one factor from different categories | Something you know/have/are |
| **Passwordless** | Sign in without a reusable password, using supported stronger methods | Passkeys/FIDO2, Windows Hello for Business |
| **Conditional Access** | Apply access rules based on signals like user, device, location and risk | If/then policy, allow/block/require MFA |
| **Azure RBAC** | Grant permissions to Azure resources at a scope | Who can read, create or manage resources |
| **External identities** | Allow guests/partners/customer identities in supported scenarios | B2B collaboration and customer access |

## Conditional Access and RBAC are different

| Conditional Access | Azure RBAC |
|:--|:--|
| Governs **sign-in conditions and access requirements** | Governs **authorised actions on Azure resources** |
| Example: require MFA for a risky sign-in | Example: assign Reader at a resource group |
| Evaluates identity/context signals | Applies role assignments at scopes |

**RBAC role assignment = security principal + role definition + scope.** Common built-in roles include **Reader**, **Contributor** and **Owner** (with very different permission levels).

## Microsoft Entra ID vs traditional Active Directory

**Microsoft Entra ID** is a cloud identity platform. It is **not just an internet-hosted replica** of classic Windows Server Active Directory Domain Services (AD DS). Applications requiring classic domain join, LDAP or Group Policy may need **Microsoft Entra Domain Services**, self-managed AD DS, or architectural changes.

> [!WARNING]
> Some sign-in monitoring and risk features exist at different licence levels. It is **not accurate** to say suspicious-sign-in detection and all related protections are always free.

> [!TIP]
> **Login attempt** → authentication / Entra ID. **Permissions after login** → authorisation / RBAC. **Require MFA under conditions** → Conditional Access. **Legacy domain features** → Entra Domain Services.

**From your notes:** Entra ID, synchronisation, Domain Services, Conditional Access and RBAC. **Syllabus supplement:** MFA, passwordless, external identities and licensing nuance.
