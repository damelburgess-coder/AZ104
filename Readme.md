README.md
evidence/
scripts/
architecture/


#Azure governance & rbac lab
##overview
This lab demonstrates Azure role-based access control (RBAC) design using separate resource groups to enforce least-privilege access.

The goal was to simulate a production environment where different users require different access levels across development and production resources.

##objectives
- we created isolated resource groups for dev and prod
- assigned different rbac roles to users
- validated least privilege access maangement
- demonstrated scope based role inheritance


#architecture
Subscription
- rg dev - UserA(contributor)
- rg prod - user b(contributor)


## Implementation Steps

1. Created resource groups:
   - `rg-dev`
   - `rg-prod`

2. Created test users in Entra ID:
   - user-dev
   - user-prod

3. Assigned roles:
   - Reader → rg-dev
   - Contributor → rg-prod


   ## Key Concepts Demonstrated

- Azure RBAC scope hierarchy
- Least privilege security model
- Role assignment boundaries
- Subscription vs resource group permissions
- Access testing and validation

---

## Lessons Learned
- RBAC is inherited downward from scope
- Contributor does not grant user management
- Reader is safe for monitoring-only access
- Resource group isolation simplifies governance


## Tools Used
- Azure Portal
- Azure CLI
- Microsoft Entra ID