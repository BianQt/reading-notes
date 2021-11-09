# Access Control (ACL)
## Preparation Materials
### RBA
Role-based access control (RBAC) is a policy-neutral access-control mechanism defined around roles and privileges. The components of RBAC such as role-permissions, user-role and role-role relationships make it simple to perform user assignments. A study by NIST has demonstrated that RBAC addresses many needs of commercial and government organizations.[4] RBAC can be used to facilitate administration of security in large organizations with hundreds of users and thousands of permissions. Although RBAC is different from MAC and DAC access control frameworks, it can enforce these policies without any complication.

#### What is a role?
One's position in a company may be referred to as a "role." But a role has a more technical definition in RBAC: it is a clearly defined set of abilities, or permissions, for use within company systems. Each internal user has at least one role assigned to them, and some may have multiple roles.

Roles are generic and are not tailored to any one employee within an organization. For example, a salesperson would not receive permissions set up specifically for their user account. Instead, they would be assigned the "salesperson" role and all accompanying permissions, such as the ability to view and edit the customer account database. Other salespeople on the team would be assigned the same role. If a specific salesperson needed expanded permissions, they would be assigned an additional role.

This approach does make adding or removing a user relatively simple — instead of editing permissions for individual users, an administrator can simply change their role.

#### What is a user permission?
In the context of access control, a permission is the ability to perform an action. One example could be the ability to upload a file to a company database. A trusted user — say, an internal employee — will have permission to upload files, while an external contractor may not have this ability. In RBAC, every possible role comes with a set of permissions.

#### RBAC vs. ABAC
Both RBAC and ABAC take into account characteristics of the user. However, ABAC can take a greater amount of context into account, such as the action being performed and properties of the data or system the user is accessing, while RBAC only takes the user's role(s) into account. This makes ABAC more dynamic than RBAC, but also more complex to manage effectively.

#### What can I do with Azure RBAC?

* Allow one user to manage virtual machines in a subscription and another user to manage virtual networks
* Allow a DBA group to manage SQL databases in a subscription
* Allow a user to manage all resources in a resource group, such as virtual machines, websites, and subnets
* Allow an application to access all resources in a resource group