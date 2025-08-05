## Last Class
- We covered injections (SQL and OS)
- I should have gotten the extra credit
	- I did get the extra credit, by being better than Tiana

### DoS
- What is DoS?
	- A DoS attack is a type of cyber attack in which a malicious actor aims to render a computer or other device unavailable to its intended users by interrupting its normal functioning
	- DoS attacks typically function by overwhelming or flooding a targeted machine with requests until regular traffic cannot be processed, resulting in a denial-of-service to additional users.
- What is Distributed DoS (DDoS)?
	- DoS attack launched from multiple systems (often infected with malware and controlled as a botnet)
	- Harder to block due to multiple sources
- Types of attacks:
	- Volume-Based Attacks: floods the network with traffic (UDP flood, ICMP flood, DNS amplification, etc.)
	- Protocol Attacks: exploits weaknesses in the protocols (SYN flood, Ping of Death, etc.)
	- Application Layer Attacks: targets app-level services (HTTP floods, Slowloris, etc.)
- Volume-Based Attacks:
	- Flood the target with massive volumes of traffic to consume bandwidth and cause network congestion
	- Examples:
		- UDP Flood: send many UDP packets to random ports
		- ICMP (Ping) Flood: overwhelms using ICMP Echo Requests
		- DNS Amplification: reflects small DNS requests into large payloads
			1. Send a small DNS request to a public DNS Server, but spoof the IP to the target IP
			2. The DNS server sends a much larger response to the spoofed IP
			3. The attacker repeats this with many servers, creating a flood of significant DNS responses
	- Mitigations
		- Rate limiting per IP or protocol
		- Deploy CDNs and DDoS protection services (Cloudflare, Akamai, etc.)
		- Block unused ports and protocols at the edge router
- Protocol-Based Attacks:
	- Exploit weaknesses in network protocols to exhaust server resources or disrupt connections.
	- Examples:
		- SYN Flood: sends many TCP SYN packets and never completes the handshake
			- Opens tons of ports waiting for ACK after send the SYN-ACK
		- Ping of Death: sends oversized ICMP packets to crash the OS
		- Smurf Attack: sends a spoofed ping to the broadcast address, causing amplification
	- Mitigations:
		- Configure firewalls to drop spoofed packets
		- Use intrusion prevention systems (IPS) that detect protocol anomalies
		- Disable IP-directed broadcasts (defense against Smurf)
- Application Layer Attacks:
	- Mimic legitimate user behavior but at scale, target the application logic to exhaust CPU, memory, or I/O
	- Examples:
		- HTTP Flood: repeated requests for heavy pages
		- Slowloris: Opens many HTTP connections but sends headers slowly
		- DNS Query Floods: target recursive DNS resolvers
			1. Attacker sends thousands of DNS queries per second to a recursive DNS server
			2. Each query is for a different domain name (real or fake) preventing caching
			3. The resolver tries to look up each query by going through the full recursive process
				1. Contact the root server
				2. Asking for the authoritative name servers
				3. Recursively builds the response
			4. This overloads the resolver:
				1. CPU usage spikes
				2. Memory used for cache fills up
				3. Response time increases, or the server crashes
	- Mitigations:
		- Rate limiting: limit DNS queries per IP or domain
		- DNS query filtering: block fake/random subdomain patterns
		- Use Anycast DNS: distribute DNS load across global nodes
		- Limit recursion: only allow trusted clients to use recursion
		- Cache tuning: increase cache size and TTL for common queries
		- DNS firewall: use solutions like DNS Response Policy Zones (RPZ)
- Regex-DoS (ReDoS):
	- You know what regex is.
	- Web applications often use them to validate form fields
	- Regular expressions are generally parsed fast. Rarely does a regular expression function slowly enough to slow down a web application.
	- Vulnerable regex patterns can be exploited by crafting input that causes catastrophic backtracking
	- malicious regexes (or evil regexes) are regular expression functions slow enough to slow down a web application.
	- Very bad ideas:
		- Nested quantifiers: `.*,.+,.{1,}`
		- Repetition with alternation: `(a|aa)+`
	- It can take seconds to minutes to evaluate long malicious strings.
	- Example:
		- `^(a+)+$` this essentially takes an $O(n)$ pattern from a single `+` and makes it $O(2^n)$ because you need to check all combinations of one or more.
	- Why is this a real problem?
		- Well it's used all over the place! Client-side and server-side.
		- If the server uses it for validation and it's inefficient, good luck.
	- Mitigation:
		- Catastrophic backtracking occurs when the regex engine tries many different permutations of the pattern before determining if a match is found. This happens when we have unbounded quantifiers (such as `*`, `+`, or `,`) and can match overlapping patterns.
			- Avoid nesting quantifiers as well!
		- Use input length requirements: don't run regex on very long inputs
		- Use regex libraries with timeout: `re.safe` in Python
		- Use simpler patterns: flatten or break up complex regex
		- Validate input before regex: apply fundamental character limits or patterns

### Final Exam
- ONE WEEK FROM TODAY
	- July 24, 1:30-3:30 PM
- Same format and number of questions
- Three essay questions
	- Follow the length questions, don't say a ton of stuff if he asks for 2 sentences.
	- Two are easy
		- Short and direct
	- One is hard
		- We need to know how to do the things
- All the multiple choice and easy questions are theory. Questions 6 is a real problem, and we need to know how to perform and solve the problem. XSS, SQL, and OS injections!
	- Know the type of attack
	- Know the approach
	- Know the mitigation
	- We won't be using BurpSuite, but you will need to describe the entire process.
- 1, 2, 3 are 10 points each
- 4 and 5 are 15 points each
- 6 is 40 points
- You don't need to join the zoom if you don't have technical issues

### Upcoming Things
- Quiz 5 is designed to help study for the final
- Assignment 4
	- Take it during the class if possible (Tuesday, July 22)
	- We need to have the following software installed and ready to go:
		- Docker
		- OWASP Juice Shop container
		- VSCode (optional, use Neovim if you're a REAL DEVELOPER)
		- BurpSuite is not required
	- This is an individual assignment
	- In this lab, we will be showing how to find the vulnerability using two approaches:
		- Static analysis
		- Dynamic analysis
	- All information will be given from security tools, we will be given outputs. We just need to analyze them. We don't need to study anything beforehand, and it is open-book (no LLMs, though).
	- All we need to know before coming into class is to have Docker and OWASP Juice Shop.
	- There will be two hours to finish