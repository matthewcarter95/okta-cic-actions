**Actions for Okta Customer Identity Cloud (formerly CIC)
**

* callMockRiskAPI.action (post-login)

Calls a public Lambda function that returns a risk result randomly from three options: 1. MFA 2. APPROVE 3. DENY.  Example {"risk": "DENY"}

The action will challenge for MFA for 1, permit for 2 and block for 3.  

* verifyEmail.action (pre-registration)

Uses a 3rd party service to validate the email of the registeration to see if it's a valid domain.  Does NOT allow plus (matt+foo@okta.com) formatting.

Requires Secret **apikey** for www.mailboxvalidator.com. 

* cdyne.action (pre-registration)

Calls a 3rd party service Cdyne to get information about the phone number used to register (usually requires custom registration)

* outboundSCIM.action (pre-registration)

Shows an outbound SCIM user create to Amazon IAM Identity Center. Requires a Secret for the access key issued by AWS.

* consentOnLogin.action / redirectConsent.action

A couple of redirect examples to a glitch page (with embedded Arengu) for consent/extended registration/progressive profile

* COMING SOON: Create unique username from given+last name
