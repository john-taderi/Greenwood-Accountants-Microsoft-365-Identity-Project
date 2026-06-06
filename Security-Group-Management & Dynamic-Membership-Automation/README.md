# Overview
As part of the Microsoft 365 identity administration project for Greenwood Accountants, I implemented Security Group management and Dynamic Group automation using PowerShell. The project involved creating departmental security groups, configuring role-based access structures, and implementing a dynamic all-staff membership group with automated membership rules.
This helped improve administrative efficiency, simplify user management, and strengthen access control processes.

#### Security Groups Created
Departmental Security Groups
The following security groups were created for organizational access management:
Security Group	                                Purpose
SG-Finance-Users	                      Finance department access
SG-HR-Users	                            Human Resources access
SG-IT-Admins	                          IT administrative privileges
SG-Management	                          Management-level access

#### Benefits
- Easier permission assignment
- Improved departmental organization
- Simplified access control management
- Better security administration

#### Dynamic Group Configuration
Dynamic Security Group
SG-All-Staff
The dynamic group was configured to automatically include all active employees based on defined membership rules in Microsoft Entra ID.

#### Key Challenges
Dynamic Group Population Delay
One major challenge encountered was the delay in dynamic membership evaluation within Microsoft Entra ID.

#### Issue Experienced
Dynamic group membership updates took approximately 5–30 minutes before users appeared in the group.

#### Cause
Microsoft Entra ID dynamic groups process membership evaluations asynchronously, which can introduce propagation delays depending on tenant size and processing load.

#### Resolution
- Verified membership rules syntax
- Allowed evaluation processing time
- Used Microsoft Entra Admin Center to monitor membership updates
- Tested with smaller user batches first

#### Key Lessons Learned
#### Technical Lessons
Through this project, I gained practical experience in:
- Microsoft Entra ID administration
- PowerShell automation scripting
- Dynamic group membership configuration
- RBAC implementation
- Bulk identity provisioning
- License management automation
- Security group administration

#### Objectives Achieved
- Create departmental Security Groups
- Implement Role-Based Access Control (RBAC)
- Configure Dynamic Membership Groups
- Automate staff grouping processes
- Improve identity and access management
- Reduce manual administrative effort
- Understand Microsoft Entra ID group evaluation behaviour

#### Conclusion
This project significantly enhanced my practical experience in Microsoft 365 administration, Microsoft Entra ID, and PowerShell automation.

By implementing user provisioning, security group management, dynamic membership rules, and automated license assignment, I gained deeper insight into enterprise identity and access management processes.

The experience also improved my understanding of automation best practices, RBAC implementation, and Microsoft 365 administrative operations in real-world environments.
