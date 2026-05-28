## SSPR Enabled
SSPR was enabled for:
Selected users/groups

Example group:

SG-All-Users

Authentication Methods Configured
I enabled the following authentication methods:

Authentication Method	                 Status
Mobile Phone	                        Enabled
Email	                                Enabled

I configure the number of Authentication Methods Required to:
- Users must provide two authentication methods before password reset is allowed.
This improves security by ensuring stronger identity verification.

Configuration Steps
# Step 1: Open Microsoft Entra Admin Center
Navigate to:
Microsoft Entra Admin Center
Protection
Password Reset

# Step 2: Enable SSPR
Under Properties:
Set Self-service password reset enabled to:
Selected

Choose the required user group.

# Step 3: Configure Authentication Methods
Under Authentication Methods:
Enable:
Mobile Phone
Email
Set: Number of methods required to reset = 2

# Step 4: Configure Registration
Under Registration:
Enable:
Require users to register when signing in = Yes
Set:
Number of days before users are asked to reconfirm = 180 days
Step 5: Save Configuration
Click:
Save
End User Testing
Test Scenario

A complete password reset test was performed using a standard user account.

Test Steps
User Registration

The test user:

Logged into Greenwood Microsoft 365
Registered:
Mobile phone number
Recovery email
Password Reset Process

The user performed the following:

Opened the password reset portal
Entered username
Verified identity using:
Email verification code
SMS verification code
Created a new password
Successfully logged in with the new password
