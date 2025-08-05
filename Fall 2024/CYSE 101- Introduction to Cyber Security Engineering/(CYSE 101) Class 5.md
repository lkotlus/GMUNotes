This class...

## Identification and Authentication
- Focusing on C from CIA.
- Identification
	- Associating an identity with a subject
- Verification
	- Confirming who you are
- Authentication
	- Establishing the validity of something, proving who you are
- Verification is the state prior to authentication. Authentication is the process.

### Authentication
- Person accessing the information is who they say they are
- Factors of identification:
	- Something you know (password)
	- Something you have (key card)
	- Something you are (biometrics)
- Passwords
	- Not the best because people hate them, and they're the easiest method to break (kinda)
- Biometrics
	- Good because everyone has it and it isn't easily stolen
	- FAR (False Acceptance Rate)
		- Rate at which you falsely accept someone
		- If someone steals my phone and the scanner accepts their face due to similarity
	- FRR (False Rejection Rate)
		- The rate at which you falsely reject the right person
		- Face ID on my phone doesn't let me in because I've lost weight
- SAML SSO
	- SAML (Security Assertion Markup Language)
		- Open standard for exchanging authentication and authorization data between parties, specifically Identity Providers (IdP) and Service Providers (SP)
	- SSO (Single Sign-On)
		- Allow users to authenticate once with an identity provider and access multiple applications or services without needing to log in again
		- Like when I use my Google account to create a discord account
	- 