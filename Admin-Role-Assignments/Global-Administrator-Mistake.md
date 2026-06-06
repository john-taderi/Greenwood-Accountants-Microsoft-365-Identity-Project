# Global Administrator Mistake
### Overview
During the initial role assignment process, excessive permissions were mistakenly assigned by granting Global Administrator access to users who only required limited administrative responsibilities.

This created security concerns to me because the Global Administrator role provides unrestricted access to all Microsoft 365 services, settings, and administrative functions.

Unnecessary Global Administrator assignments included:
- Helpdesk-related tasks
- User password management
- Teams management
- Exchange mailbox administration

These tasks did not require full organizational control.
I understand that assigning unnecessary Global Administrator privileges can lead to the following:
- Increased security risks
- Accidental configuration changes
- Unauthorized access to sensitive settings
- Higher exposure to compromised administrator accounts
- Violation of least privilege security principles

### Correct Role Scope Verification Process

To correct the issue, I implemented role scope verification process. 

Step 1: Review Job Responsibilities

Each administrator’s responsibilities were reviewed to determine the exact permissions required for their role.
- Password management → User Administrator
- Mailbox management → Exchange Administrator
- Teams management → Teams Administrator

Step 2: I apply Least Privilege Principle
- Users were reassigned to lower-privileged administrative roles instead of Global Administrator whenever possible.
- Only authorized senior administrators retained Global Administrator access.

Step 3: Verify Assigned Permissions
- Each assigned role was tested to confirm:
- Required administrative tasks could be performed
- Unauthorized functions remained inaccessible
- Permission boundaries worked correctly

Step 4: Remove Excessive Privileges
Unnecessary Global Administrator assignments were removed to reduce security exposure.

### Conclusion
The incorrect assignment of Global Administrator privileges highlighted the importance of proper role scope verification. By implementing least privilege access and assigning role-specific permissions, the organization improved security, accountability, and administrative efficiency within the Microsoft 365 environment.
