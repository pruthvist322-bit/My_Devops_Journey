  Day 20 – AWS IAM (Identity and Access Management)

Today I continued my AWS learning and explored IAM, which is one of the core AWS services used to manage access and permissions securely.

Topics Covered:

• What is IAM

IAM (Identity and Access Management) is an AWS service used to securely manage users, groups, roles, and permissions for accessing AWS resources.

---

Why IAM is Used

* Secure AWS account access
* Control permissions
* Manage users and groups
* Apply least privilege access
* Improve security and auditing

---

IAM Users

IAM Users are individual identities created inside AWS with specific access permissions.

Steps Learned:

* Open AWS Console
* Search IAM
* Create User
* Assign permissions
* Configure access

---

IAM Groups

IAM Groups allow assigning permissions to multiple users together.

Benefits:

* Easier permission management
* Centralized access control

---

Permissions

Permissions define what actions users or groups can perform inside AWS.

Permissions can be attached:

* Directly to Users
* Through Groups
* Through Roles

---

Inline Policies

Inline Policies are custom policies directly attached to a single User, Group, or Role.

Features:

* One-to-one relationship
* Used for specific permission requirements
* Cannot be reused across multiple entities

Steps Learned:

* Create Inline Policy
* Define permissions
* Attach to User / Group / Role

---

Attaching Inline Policies

Learned how to:

* Select User / Role
* Open Permissions
* Create Inline Policy
* Attach policy to required resource

---

ARN (Amazon Resource Name)

ARN is a unique identifier used by AWS to identify resources.

Example:

arn:aws:service:region:account-id:resource

ARN helps AWS know exactly which resource permissions apply to.

---

Modify Inline Policies

Steps:

* Open IAM
* Select User / Group / Role
* Permissions
* Edit Inline Policy
* Update permissions

---

IAM Roles

IAM Roles provide temporary access permissions to AWS services.

Why IAM Roles are Created:

* Avoid storing credentials
* Secure service-to-service communication
* Temporary permission access
* Used by EC2, Lambda, and AWS services

---

Difference Between IAM Role and IAM Policy

IAM Role:

* Identity with permissions
* Assumed temporarily

IAM Policy:

* Collection of permission rules
* Attached to Users, Groups, or Roles

---

Key Learning:

IAM is the foundation of AWS security and access management. Proper use of Users, Groups, Policies, and Roles helps secure cloud infrastructure.


