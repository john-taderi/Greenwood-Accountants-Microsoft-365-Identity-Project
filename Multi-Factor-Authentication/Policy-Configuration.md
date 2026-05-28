## Policy Overview
The Conditional Access policy was configured to require MFA for all users accessing cloud applications for Greenwood.

## Policy Scope
Included Users
   - All organizational users included
Included Cloud Apps
   - All cloud applications
Access Control
   - It requires Multi-Factor Authentication

## Conditional Access Logic
IF user signs into Greenwood Microsoft 365 tenant
AND accesses any cloud application
THEN require MFA verification

## MFA Authentication Methods
The Primary Authentication Method used:
# Microsoft Authenticator App
The Microsoft Authenticator application was configured as the preferred MFA method because it provides:
- Push notification approval
- Number matching verification
- Stronger security protection
- Faster authentication experience

## Fallback Authentication Method
# SMS Authentication
I configured SMS verification as a fallback option for users unable to install Microsoft Authenticator.

Reasons for SMS Fallback
- Incase of unsupported mobile devices
- It limited smartphone access
- It allows temporary onboarding limitations

## MFA Rollout Strategy
Rollout Phases include
# Phase 1 – Pilot Testing
Initial rollout was performed with:
- IT administrators
- Test accounts
- Early adopters

#  Phase 2 – Departmental Rollout
I expanded the MFA enforcement to:
- Finance Department
- HR Department
- Management Team

# Phase 3 – Organization-wide Enforcement
MFA policy fully enforced for all users.

## MFA Registration Process
User Registration Steps

I instructed the users to:
- Sign in to Microsoft 365
- Register Microsoft Authenticator
- Add phone number for SMS fallback
- Complete MFA verification setup

## Challenges Encountered
   # MFA Registration Challenges
Some users experienced difficulties during MFA registration due to unfamiliarity with Microsoft Authenticator setup.

Impact of the challenges on the users
- The enrollment process was delayed
- There is increased support requests from users
- Users onboarding resistance
  
   # What I do to resolve the challenges
- I Provided user onboarding guidance
- I Shared MFA setup instructions
- I assisted users during registration process

   # SMS Fallback Limitations
SMS authentication presented several limitations:
- Delayed OTP delivery
- Mobile network dependency
- Lower security compared to Authenticator App
  # How I Resolved the limitations
- I positioned SMS strictly as a backup method
- I encouraged users to adopt Microsoft Authenticator
- I educated users on secure MFA practices

## Challenges of Conditional Access Policy Lockout Risk
Incorrect conditional access configuration could potentially lock administrators out of the environment.
# I do this as resolution
- Configured break-glass administrator accounts
- Tested policies before full deployment
- Applied staged enforcement approach

## Challenges of Policy Propagation Delay
Conditional access policies required propagation time before taking full effect across the environment.
# I resolved to:
- Allowed synchronization time
- Verified enforcement using sign-in logs
- Performed validation testing

## Key Lessons Learned
Through this hand-on project, I gained practical experience in:

- Microsoft Entra ID Conditional Access
- MFA deployment and management
- Microsoft Authenticator configuration
- Identity protection strategies
- Azure AD security operations
- Authentication policy enforcement

## Conclusion
- This project significantly improved my hands-on experience in Microsoft Entra ID security administration and enterprise identity protection.

- By implementing Conditional Access policies, MFA enforcement, and fallback authentication methods, I gained practical knowledge of securing Microsoft 365 environments using Zero Trust principles and modern authentication controls.

- The project also enhanced my understanding of user onboarding strategies, security governance, and cloud identity management best practices.
