# Access Control

## RBAC definition

RBAC is the idea of assigning system access to users based on their role within an organization. The system needs of a given workforce are analyzed, with users grouped into roles based on common job responsibilities and system access needs.

## Benefits of RBAC?

the assignment of access rights becomes systematic and repeatable. Further, it is much easier to audit user rights, and to correct any issues identified.
RBAC may sound intimidating, but it can in reality be easy to implement, and will make the ongoing management of access rights much easier and more secure.

## RBAC vs. ABAC vs. ACL

- Access control lists (ACL) — An ACL is a means of defining access rights by a given user or user group, to a specific object, such as a document.

- Attribute-based access control (ABAC) — ABAC, sometimes known as policy-based access control, can use a variety of attributes, including user department, time of day, location of access, type of access required, etc. to determine whether a user’s access request should be granted.

**Three primary rules are defined for RBAC:**

Role assignment: A subject can exercise a permission only if the subject has selected or been assigned a role.
Role authorization: A subject's active role must be authorized for the subject. With rule 1 above, this rule ensures that users can take on only roles for which they are authorized.
Permission authorization: A subject can exercise a permission only if the permission is authorized for the subject's active role. With rules 1 and 2, this rule ensures that users can exercise only permissions for which they are authorized.

**The NIST/ANSI/INCITS RBAC standard (2004) recognizes three levels of RBAC:**

core RBAC
hierarchical RBAC, which adds support for inheritance between roles
constrained RBAC, which adds separation of duties.
