# Awesome-User-Provisioning-Directory-Services

## Top User Provisioning & Directory Services Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Identity Lifecycle Automation, Directory Management & Self-Hosted IAM*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **User Provisioning & Directory Services**. These tools enable organizations to automate the joiner-mover-leaver lifecycle—creating, updating, and revoking user access across applications based on HR data and directory group memberships—while maintaining a centralized source of truth for identities and enforcing least privilege.



**Examples** include Atlassian User Management, Okta Lifecycle Management, Microsoft Entra ID, JumpCloud, OneLogin, SailPoint, Lumos, Rippling, BetterCloud, and CyberArk Identity (the category leaders).



**Open-source emphasis**: User Provisioning & Directory Services is a domain where open-source tooling is **strong at the directory and IAM layers but requires assembly for full lifecycle automation**. The strongest active projects are **Keycloak**, **Casdoor**, and **WSO2 Identity Server** for IAM with SCIM provisioning , **Axia** for LDAP/AD management with role-based access and audit logs , and **FusionDirectory** for delegated LDAP directory administration with trigger-based automation . For SCIM specifically, **GoSCIM** provides a lightweight, RFC-compliant SCIM 2.0 server , and **Canaille** offers lightweight identity management with SCIM provisioning . The critical gap: **no open-source project replicates the turnkey HR-to-app orchestration** of Okta or Rippling—those require building the orchestrator and connectors yourself.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Atlassian User Management](https://www.atlassian.com/)**  

  Native user and group management across Atlassian products (Jira, Confluence, Bitbucket); supports SCIM provisioning from identity providers, role assignments, and product access controls.



- **[Okta Lifecycle Management](https://www.okta.com/)**  

  Leading identity cloud with automated provisioning/deprovisioning via SCIM and HR-driven workflows across thousands of app integrations; the benchmark for turnkey user lifecycle automation.



- **[Microsoft Entra ID](https://www.microsoft.com/en-us/security/business/microsoft-entra)**  

  Microsoft's cloud identity service with Lifecycle Workflows (joiner/mover/leaver triggered by HR events), entitlement management, access reviews, and SCIM provisioning to SaaS apps.



- **[JumpCloud](https://jumpcloud.com/)**  

  Cloud directory platform with Directory-as-a-Service lifecycle management, SSO, device management, and LDAP; automates user onboarding/offboarding across connected systems.



- **[OneLogin](https://www.onelogin.com/)**  

  Identity and access management platform (now part of One Identity) with SSO, MFA, and automated user provisioning workflows.



- **[SailPoint](https://www.sailpoint.com/)**  

  Identity governance and administration (IGA) leader with access certification, role mining, lifecycle management, and compliance reporting.



- **[Lumos](https://www.lumos.com/)**  

  Identity governance platform focused on app access requests, approvals, and automated provisioning; positioned for mid-market companies wanting governance without full IGA complexity.



- **[Rippling](https://www.rippling.com/)**  

  Unified HR/IT platform with Identity and Access Management built on a single Employee Graph; automates onboarding/offboarding and enforces role-based access across 650+ integrations.



- **[BetterCloud](https://www.bettercloud.com/)**  

  SaaS management platform with automated user lifecycle workflows, policy enforcement, and directory integration for multi-app environments.



- **[CyberArk Identity](https://www.cyberark.com/)**  

  Identity security platform with privileged access management and identity governance; enforces least privilege across provisioning workflows.



## Open-Source GitHub Projects



### Full IAM Platforms with SCIM Provisioning



- **[Keycloak](https://github.com/keycloak/keycloak)**  

  The most widely adopted open-source IAM platform (Apache-2.0); provides SSO, OAuth 2.0, OIDC, SAML, LDAP, RBAC, and **SCIM 2.0 server support (since 26.8)** for receiving users from Entra ID or Okta . User federation and identity brokering included. **The default choice for self-hosted IAM**—but provisioning workflows beyond SCIM ingestion require custom development.



- **[Casdoor](https://github.com/casdoor/casdoor)**  

  UI-first open-source IAM/SSO platform (Apache-2.0) with OAuth 2.0, OIDC, SAML, CAS, LDAP, and RBAC; includes **SCIM 2.0 server** (users and groups), a **built-in LDAP server**, and **MCP server** for AI agent access . Supports 70+ social/enterprise identity providers and syncers for Keycloak, Okta, Entra ID, Active Directory, Google Workspace, and any SQL database . **The most feature-dense open-source IAM for directory integration**—Go-based with a clean admin UI.



- **[WSO2 Identity Server](https://github.com/wso2/product-is)**  

  Enterprise-grade open-source IAM (Apache-2.0) recognized as a Digital Public Good; supports OAuth2, OIDC, SAML, SCIM 2.0, FIDO2, adaptive MFA, and RBAC. Manages over 1 billion identities across 1,500+ commercial deployments. **The most enterprise-ready open-source IAM foundation** for provisioning and SSO.



- **[Hanzo IAM](https://github.com/hanzoai/iam)**  

  Open-source, AI-first IAM with web UI (Apache-2.0); supports OAuth 2.1, OIDC, SAML, CAS, LDAP, **SCIM provisioning**, WebAuthn, MFA, RBAC, and multi-tenancy . **Notable for MCP/A2A gateway** for AI agent access control. A modern alternative for teams building AI-augmented identity workflows.



### Directory Management (LDAP / Active Directory)



- **[Axia](https://github.com/Nelsar/Axia)**  

  Self-hosted **LDAP admin web console and REST API** for Active Directory and OpenLDAP (MIT) . Features user, group, OU, and computer management with **role-based access** (Admin, UserCreator, UserEditor, UserDeleter) and **audit logging**; LDAPS with certificate verification, JWT-based API auth, AES-encrypted bind passwords at rest, and PostgreSQL/SQLite backend. Docker Compose deployment or Windows installer. **The cleanest open-source LDAP management tool** for administrators wanting a modern web UI over directory operations—but it manages the directory, not cross-app provisioning.



- **[FusionDirectory](https://github.com/fusiondirectory/fusiondirectory-plugins)**  

  Open-source **Identity Management solution for LDAP directories** (GPL) . Provides delegated administration with fine-grained ACLs and complex roles (User, Local admin, Global admin, HR); manages users, groups, mail, sudo, ssh, systems, services, DHCP, and DNS. **Trigger system** launches scripts on create/edit/delete/password-change events—useful for automating onboarding/offboarding actions (badge generation, mailbox archiving, third-party app deletion) when a user is added or removed from LDAP . **The strongest open-source tool for delegated directory administration with event-driven automation**.



- **[GLAuth](https://marketplace.microsoft.com/en-us/product/athinfosystems1641442221349.glauth)**  

  Lightweight open-source **LDAP authentication and identity management server** written in Go . Positioned as a simple alternative to OpenLDAP and Microsoft Active Directory; supports centralized user/group management, file-based or database-backed directories, REST API, web administration, and role-based access control. Container-friendly with Docker/Kubernetes support. **Best for small to mid-sized environments** wanting a minimal LDAP server without full AD complexity .



### SCIM Provisioning Servers



- **[GoSCIM](https://github.com/arturoeanton/goscim)**  

  Lightning-fast **SCIM 2.0 server** in Go (RFC 7643/7644 compliant) . Features dynamic schema loading (add resource types via JSON, no code), per-attribute permissions, OAuth 2.0, ETag concurrency control, and Couchbase backend. **Limitations**: no Bulk operations, no value-path filters, no password hashing . **The best lightweight SCIM server** for building custom provisioning endpoints—pair with an orchestrator for lifecycle automation.



- **[Canaille](https://pypi.org/project/Canaille/0.0.77/)**  

  Lightweight identity and authorization management software (Python) . Features user profile and group management, authentication/registration/password reset, authorization via OpenID Connect, and **SCIM provisioning**; first-class support for PostgreSQL, MariaDB, and OpenLDAP; customizable and themable . **Best for teams wanting a simple, readable identity management layer** with SCIM output.



### Additional Strong Open-Source Options



- **FreeIPA** — Open-source identity management for Linux environments (LDAP, Kerberos, policy-based access control); can integrate with AD for mixed environments . **Linux-centric**—best for organizations standardizing on Linux infrastructure.

- **OpenLDAP** — The foundational open-source LDAP directory server; integrates with AD for authentication and directory queries . **Infrastructure layer**—provides the directory itself, not management tooling or provisioning workflows.

- **Apache Directory Studio** — GUI-based LDAP directory editor for browsing, editing, and schema management . **Administrator tool**—useful for manual directory operations, not automated provisioning.



**Frameworks for building custom systems**: For **IAM with SCIM ingestion and SSO**, Keycloak, Casdoor, or WSO2 Identity Server . For **LDAP/AD management with audit logs**, Axia . For **delegated directory administration with event-driven automation**, FusionDirectory . For **lightweight SCIM endpoints**, GoSCIM . For **simple identity management with SCIM output**, Canaille . No open-source project provides the **turnkey HR-to-app orchestration with pre-built connectors** of Okta or Rippling—that requires assembling an orchestrator (like the hr-onboarding-automation reference) with SCIM servers and directory management tools.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- User provisioning and directory services platforms handling identity data must comply with applicable privacy regulations (GDPR, CCPA) and security frameworks (SOC 2, ISO 27001); **improper deprovisioning leaves orphaned accounts that create breach risk**.

- **Open-source user provisioning is mature at the IAM and directory layers**—Keycloak, Casdoor, and WSO2 Identity Server provide production-grade identity and SCIM capabilities , and Axia/FusionDirectory provide directory management with audit trails . However, **no open-source project replicates the turnkey HR-driven lifecycle automation** of Okta or Rippling with pre-built connectors for hundreds of apps. Organizations requiring full lifecycle automation should evaluate commercial platforms or invest in custom orchestration.

- Verify license terms for commercial use; Keycloak and Casdoor use Apache-2.0 , Axia uses MIT , FusionDirectory uses GPL , and GoSCIM is open-source (check repository) .



---



**Made for identity architects, IT administrators, security engineers, and directory services teams.**  

Let's make user provisioning and directory services more open, but with clear eyes about the connector ecosystem and lifecycle orchestration that commercial platforms still own.
