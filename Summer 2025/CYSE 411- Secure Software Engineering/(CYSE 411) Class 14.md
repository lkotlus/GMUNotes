### BurpSuite
- Basic usage stuff

### CSRF
- Cross-Site Request Forgery
- Second threat we're studying in this course (first was XSS)
- Definition:
	- CSRF is an attack that tricks a user's browser into executing unwanted actions in a web application in which they are authenticated
	- Key point: exploits the trust a web application has in the user's browser
- What is "cross-site"?
	- Refers to a situation where a web request originates from a different origin (site) than the destination. In web security, an "origin" is defined by:
		- Protocol
		- Domain name
		- Port number
- Essentially, you leverage the trust that a server has in a particular user to execute actions on that user's behalf. 
- For example, a fake banking webpage where you attempt an action, and I redirect you to the real one and have you send me money.
- XSS leverages user trust in content, CSRF leverages server trust in user.
- How it works:
	1. User logs into trusted site (website A)
	2. User stays logged in (session cookie present)
	3. Attacker sends a malicious link or form to website B
	4. Browser sends a request to website A with valid credentials
	5. Website A performs the action, assuming it came from the user
- This can be done via:
	- POST requests from forms
	- `img` tags with malicious `src` attributes (can also be done with videos)
	- Invisible buttons on forms
- Why it works:
	- Browsers automatically include cookies in same-origin requests
	- Server trusts the session without verifying the request origin
	- Users are often logged in to multiple services
- Mitigation Techniques
	- CSRF Token
		- A CSRF token is a randomly generated secret value that is:
			- Tied to the user's session
			- Included as a hidden field in HTML forms or HTTP headers
			- Verified on the server-side for every state-changing request (POST, PUT, DELETE, etc.)
			- The token ensures that the request originated from the legitimate user interface and not from a malicious site
	- `SameSite` cookie
		- A cookie attribute introduced by browsers to control whether cookies are sent with cross-site requests.
		- They have three modes:
			- `Strict`: cross-site GET and POST are blocked
			- `Lax`: cross-site POST is blocked
			- `None`: everything is allowed, must be used with `Secure`
	- Double Submit Cookies
		- Double Submit Cookies is a CSRF mitigation technique that doesn't require storing tokens on the server side
		- Instead, the CSRF token is:
			- Set as a cookie (like a normal session cookie)
			- Sent again in a custom HTTP header or form field
		- The malicious site can trigger a request, but it can't read the CSRF token from the cookie because of the Same-Origin Policy
	- Referer and Origin Headers
		- When a browser sends a request to a web server, it often includes one or both of the following headers:
			- `Referer`: the full URL of the page where the request originated
			- `Origin`: Just the protocol + hostname + port
			- These headers help the server identify the source of a request
			- Server sees mismatch in origin and referer -> reject the request
	- 