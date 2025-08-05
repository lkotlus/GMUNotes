### Midterm Last Class
- That sucked

### Threat Analysis
- Recall the steps of threat modeling:
	1. System Modelling (DFD)
	2. Threat Enumeration (STRIDE)
	3. Ranking Threats (Threat Analysis Part 1)
	4. Countermeasures and Mitigations (Threat Analysis Part 2)
- What is threat ranking?
	- Threat ranking is identifying and measuring the negative consequences of a threat being exploited. 
	- We aim to create a prioritized list of threats to support a risk mitigation strategy, such as prioritizing the more critical threats.
	- We need a method to prioritize threats based on
		- Impact
		- Likelihood
		- Exposure
	- Helps determine which risks to mitigate first
- What is risk?
	- Risk is the probability of something suffering harm or loss
	- An effect of uncertainty on or within information and technology
- Threat Ranking Models
	- DREAD
		- Semi-quantitative scoring of threats
		- Focuses on technical risk
	- OWASP Risk Rating
		- $\text{risk}=\text{likelihood}\cdot\text{impact}$
		- Focuses on AppSec/DevSecOps
	- CVSS
		- Standard for scoring vulnerabilities
		- Focuses on industry and compliance
	- FAIR
		- Financial quantitative risk analysis
		- Focuses on business and enterprise
	- Custom Risk Matrix
		- A 2D grid: likelihood vs. impact
		- Focuses on simplified risk ranking
- We will frequently use multiple to cover our bases. Using DREAD and OWASP Risk Rating will help to see things from multiple perspectives.
- It can be difficult to measure all risk in dollar amounts:
	- Privacy (**<u>sometimes</u>**)
	- Critical infrastructure
	- National security

### Microsoft DREAD
- Risk assessment model used in threat modeling.
- Prioritizes threats based on five key criteria
- Each criterion is scored, and the scores are summed or averaged
- Developed by the MS SDL team, but no longer used due to subjectivity
- Criteria
	- Damage: how bad would an attack be?
	- Reproducability: how easy is it to reproduce the attack?
	- Exploitability: how much work is it to launch the attack?
	- Affected users: how many people will be impacted?
	- Discoverability: how easy is it to discover the threat?
- Bug bars (just an example)!
	- Assuming we rank everything from 0-10
	- Damage
		- 0: no damage
		- 5: information disclosure
		- 8: non-sensitive user data about individuals or employers have been compromised
		- 9: non-sensitive administrative data was compromised 
		- 10: destruction of an information system; the inaccessibility of data, or applications
	- Reproducability
		- 0: difficult or impossible
		- 5: complex
		- 7.5: easy
		- 10: very easy
	- Exploitability
		- 2.5: advanced programming and networking skills
		- 5: available attack tools
		- 9: web application proxies
		- 10: web browser
	- Affected users
		- 0: no users
		- 2.5: individual user
		- 6: few users
		- 8: administrative users
		- 10: all users
	- Discoverability
		- 0: hard to discover
		- 5: HTTP request can uncover it
		- 8: can be found in the public domain
		- 10: vulnerability found in web address bar or form
- Measuring things with an average is: $$\frac{\sum \text{ratings}}{5}$$
- So if we have a 5 D, R, E, A, and D: $$\frac{5+5+5+5+5}{5}=\frac{25}{5}=5$$
- Ratings from scores

|Rating|Score (sum)|Score (average)|
|-|-|-|
|High|40-50|8-10|
|Medium|25-39.9|5-7.9|
|Low|0-24.9|0-4.9|

### Common Vulnerability Scoring System (CVSS)
- Standardized framework used to rate the severity of vulnerabilities
- Developed by FIRST.org, widely used in:
	- NIST's National Vulnerability Database (NVD)
	- Security tools and scanners
	- Vulnerability management platforms
- Scores range from 0.0 to 10.0
- Three metrics:
	- Base metrics
		- Intrinsic characteristics of the vulnerability
	- Temporal metrics
		- Characteristics that may change over time (such as exploit availability)
	- Environmental metrics
		- Tailored to a specific environment or aspect
- Most public CVSS scores only use the base score
- Base metric group
	- Access vector (network, adjacent, local, physical, etc.)
	- Attack complexity (low, high, etc.)
	- Privileges required (none, low, high, etc.)
	- User interaction (none, required, etc.)
	- Scope (unchanged, changed, etc.)
		- Unchanged: the vulnerable component and impacted component are the same
			- Example: SQL injection leaks data in the same web app.
		- Changed: the impact crosses a security boundary
			- Example: exploiting a web server to execute code in the OS or escalating privileges
	- Impact (none, low, high (confidentiality, integrity))
- Temporal metric group
	- Exploitability
	- Remediation level
	- Report confidence
- Environmental metric group
	- Collateral damage potential
	- Target distribution
	- Confidentiality requirement
	- Integrity requirement
	- Availability requirement
- Understanding CVSS scores:
	- CVSS base score is calculated using a detailed mathematical formula that combines:
		- Exploitability metrics (AV, AC, PR, UI, etc)
		- Impact metrics (C, I, A)
		- Scope (S)
	- Easiest to just use the calculator that they have online

### Threat Treatment
- What is it?
	- Threat treatment is a general term that refers to actions taken to manage or mitigate risks
	- The goal is to minimize the impact of potential security incidents
- The big 4
	- Accept
		- We will tolerate the consequences and take no proactive actions
	- Avoid
		- Activities are restructured to eliminate the possibility of a threat exploitation occurring
	- Transfer
		- Shift the threat mitigation to another party (insurance or outsourcing). 
		- The system owner always retains responsibility for managing the risk, even if it is transferred.
	- Reduce
		- Actions are implemented to reduce or contain threats

### Risk Matrices
- A risk matrix is a visual tool for evaluating and prioritizing potential risks
- It's also known as a probability and severity matrix, or a likelihood and impact matrix.
![[Pasted image 20250626144844.png]]
- We can Also have more combination based matrices, as used in Europe:
![[Pasted image 20250626144936.png]]
![[Pasted image 20250626145002.png]]

### Countermeasures and Mitigations
- Mitigation involves applying countermeasures in order to:
	- Reduce likelihood (exploit becomes harder)
	- Reduce impact (damage is limited)
- The purpose is to determine if some protective measure can prevent a threat from being realized
- Some selection criteria
	- Risk appetite of the organization
	- Cost and benefit of mitigation (if the exploit costs less than the mitigation, don't do anything)
	- Legal and compliance obligations
- Types of security controls
	- Preventative: stop an attack before it happens (firewalls, access control, code signing, etc.)
	- Detective: identify threats that are occurring (monitoring, anomaly detection, logging, etc.)
	- Corrective: limit damage and restore service (backup stores, patching, system reboots, etc.)
- Controls by SDL phase
	- Design
		- Type of control: preventative (architectural)
		- Description: controls that are built into the system architecture to prevent threats
		- Example: secure software design, principle of least privilege, etc.
	- Implementation
		- Type of control: preventative (technical)
		- Description: controls added during development or configuration
		- Example: input validation, authentication, encryption, etc.
	- Operational
		- Type of control: detective/reactive
		- Description: controls that monitor, detect, or respond to threats
		- Example: IDS, audit logs, SIEM alerts, incident response, etc.
- STRIDE
	- Controls must align with the corresponding threat category
	- A good system design includes layers of defense across the STRIDE categories
		- Use defense-in-depth: combine preventive + detective + corrective whenever possible
		- You can't protect against spoofing with logging alone - you need strong authentication
	- There's a table in the slides.

### Homework
- Assignment 3!
- Group activity. We're performing threat analysis.
- We need to:
	1. Create a DFD
	2. STRIDE per-element enumeration
	3. DREAD ranking
	4. ...
	5. Matrices
	6. Mitigations
- After that, we need to create a report. This is done through Threat Dragon, we need to submit a PDF and the JSON.
- 80% of the grade is the submission, 20% is the peer evaluation.