# Lab 02: Microsoft Entra ID — User Lifecycle Management

## Objective

Practice identity lifecycle management in Microsoft Entra ID, focusing on employee onboarding, access modifications, and offboarding.

**Environment:** Microsoft Entra ID | Ohana Lab Tenant

## 1. Security Group Creation

Created three security groups with assigned membership to organize employees by department:

- SG-Cybersecurity
- SG-HR
- SG-IT-Support

![Security group creation](screenshots/01-group-creation.png)

*Figure 1: Configuring a security group with assigned membership.*

![Security groups](screenshots/02-security-groups.png)

*Figure 2: Three security groups successfully created.*

## 2. Employee Onboarding

Assigned three employees to their respective security groups:

**Amara Lewis — Cybersecurity**

![Amara membership](screenshots/03-amara-membership.png)

*Figure 3: Amara Lewis assigned to SG-Cybersecurity.*

**Sofia Martinez — Human Resources**

![Sofia membership](screenshots/04-sofia-membership.png)

*Figure 4: Sofia Martinez assigned to SG-HR.*

**Ethan Brooks — IT Support**

![Ethan membership](screenshots/05-ethan-membership.png)

*Figure 5: Ethan Brooks assigned to SG-IT-Support.*

## 3. Access Modification — Ethan Brooks

**Scenario:** Ethan transfers from IT Support to Cybersecurity.

Updated his job title to Security Analyst and department to Cybersecurity.

![Ethan department change](screenshots/06-ethan-department-change.png)

*Figure 6: Updating Ethan's job information.*

Added Ethan to SG-Cybersecurity to reflect his new department.

![Ethan Cybersecurity membership](screenshots/07-ethan-cybersecurity.png)

*Figure 7: Ethan and Amara listed as Cybersecurity group members.*

**Security principle:** Group memberships should be reviewed whenever an employee changes roles to prevent unnecessary access.

## 4. Employee Offboarding — Sofia Martinez

**Scenario:** Sofia leaves the organization.

### Disable Account

Configured Sofia's account to prevent further sign-ins.

![Sofia account disabled](screenshots/08-sofia-disabled.png)

*Figure 8: Disabling Sofia's Entra ID account.*

### Revoke Sessions

Initiated session revocation to invalidate Sofia's existing sign-in sessions.

![Sofia sessions](screenshots/09-sofia-revoke-sessions.png)

*Figure 9: Session revocation confirmation prompt.*

### Remove Group Membership

Removed Sofia from SG-HR.

![Sofia group removal](screenshots/10-sofia-removed.png)

*Figure 10: SG-HR showing zero members after Sofia's removal.*

## 5. Security Concepts Practiced

- Identity and Access Management (IAM)
- User lifecycle management (Joiner–Mover–Leaver)
- Security group management
- Role-based access principles
- Least privilege
- Account disabling and session revocation

## 6. Key Takeaways

Microsoft Entra ID enables administrators to manage user identities throughout their employment lifecycle. Updating memberships when roles change and revoking access during offboarding helps reduce the risk of unauthorized access.

**Reference:** [Microsoft Learn — Create and manage users and groups](https://learn.microsoft.com/en-gb/training/modules/configure-entraid-device-management/03-create-manage-users-groups)
