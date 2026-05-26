# Identity Strategy Design Document
## Overview 
Greenwood Accountants is implementing a structured identity and access management solution using Microsoft Entra ID to manage.
- user access
- departmental permissions
- license assignments
- collaboration
- automated identity governance

The environment is designed to support:
Finance
Human Resources (HR)
Information Technology (IT)
Sales
Management Departments

## Objectives of the Group Design
The group structure is designed to achieve the following objectives:
- Centralized access management
- Simplified administration
- Role-based access control (RBAC)
- Automated user grouping
- Improved security
- Easier license assignment
- Scalability for future growth
- Departmental separation of access

## Group Design Standards
# Naming Convention
The following naming standards are used:
Prefix                  Meaning
SG                  Security Group
M365                Microsoft 365 Group
DG                  Dynamic Group

<Examples:>
SG-Finance-Users
SG-IT-Admins
SG-All-Staff

## Security Group Structure
# Finance Department Group
Group Name
- SG-Finance-Users
Group Type
- Security Group
  
# Purpose
Provides Finance department users with:
- accounting application access
- finance SharePoint access
- payroll system permissions
- Membership Type
- Assigned Membership
  
# Members
- Finance department staff only.

## Human Resources Group
Group Name
- SG-HR-Users
Group Type
- Security Group
# Purpose
Provides HR staff with:
- HR application access
- employee record permissions
- HR document access
- Membership Type
- Assigned Membership

## IT Administration Group
Group Name
- SG-IT-Admins
  Group Type
  - Security Group

# Purpose
Provides IT administrators with:
- elevated administrative permissions
- device management access
- system administration privileges

# Membership Type
Assigned Membership

## Security Note
Membership should be tightly controlled due to privileged access.

## Management Group
Group Name
- SG-Management

Group Type
- Security Group
Purpose
Provides management staff with:
- executive resource access
- management reporting tools
- strategic document access
- 
Membership Type
- Assigned Membership

## Dynamic Group Structure
All Staff Dynamic Group
Group Name
- SG-All-Staff

Group Type
- Dynamic Security Group

# Purpose
Automatically groups all employees across departments.
Dynamic Membership Rule
(user.department -eq "Finance") or
(user.department -eq "HR") or
(user.department -eq "IT") or
(user.department -eq "Sales") or
(user.department -eq "Management")

Membership Type
- Dynamic Membership
Use Cases
- company-wide communications
- license assignment
- Conditional Access policies
- organization-wide application access

## Recommended Microsoft 365 Collaboration Groups
The following Microsoft 365 groups are recommended for collaboration purposes:
Group Name                                   Purpose
M365-Finance-Team                       Finance collaboration
M365-HR-Team                            HR collaboration
M365-Management-Team                    Executive collaboration

These groups provide:
- Teams integration
- shared mailbox
- shared calendar
- SharePoint site
- Planner access

## User-to-Group Mapping
Department                         Assigned Group
Finance                           SG-Finance-Users
HR                                SG-HR-Users
IT                                SG-IT-Admins
Management                        SG-Management
All Departments                   SG-All-Staff

## Access Control Strategy
The organization adopts Role-Based Access Control (RBAC) principles.
Access is granted:
- based on department
- based on job role
- through group membership instead of direct user assignment

# Benefits:
- easier auditing
- simplified administration
- reduced configuration errors
- improved scalability

## License Assignment Strategy
Licenses are assigned using group-based licensing.
Recommended assignment:
SG-All-Staff
→ Microsoft 365 Business Premium license

# Benefits:
- automatic onboarding
- simplified administration
- reduced manual errors

## Dynamic Group Processing Consideration

# Dynamic group membership updates are not immediate.
Expected evaluation delay:
5–30 minutes

This may temporarily affect:
- license assignment
- Teams access
- Conditional Access enforcement

# Mitigation:
- allow synchronization time
- verify attribute consistency
- monitor membership processing

## Security Recommendations
- Least Privilege Principle
- Users should receive only the minimum access required.

## Administrative Group Protection
The following groups require restricted membership:
- SG-IT-Admins
- SG-Management
  
# Recommended controls:
- Privileged Identity Management (PIM)
- MFA enforcement
- Conditional Access policies

## Naming Governance
Maintain consistent naming standards for:
- clarity
- automation
- reporting
- scalability

## Scalability Considerations
The design supports future expansion, including:
- additional departments
- regional offices
- device groups
- application-specific groups
- hybrid identity integration

## Conclusion
The Greenwood Accountants group structure design provides:
- secure identity management
- scalable access control
- automated user organization
- simplified administration
- improved governance

By combining:
- Security Groups
- Dynamic Groups
- Microsoft 365 Groups
the organization achieves a modern, manageable, and secure Microsoft Entra ID environment.





