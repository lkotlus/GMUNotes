### Second Part of the Course!
- Finally.

### Chrome Developer Tools
- Easy. EASY.
- Today is cruise control. We might get into some XXS.

### Architecture
- Monolithic
	- Single codebase containing all application components
	- Pros: simple to develop and easy to deploy
	- Cons: difficult to scale and maintain as the application grows
- Three Tier
	- Presentation layer
		- Handles interactions
		- HTML, CSS, JS Frameworks
	- Business layer
		- Processes user requests and applies business rules
		- Server-side languages (Java, Python, NodeJS)
	- Data Layer
		- Manages data operations
		- SQL (MySQL, PostgreSQL, etc.) or NoSQL (MongoDB, DynamoDB, etc.)
	- Much better or security, as we have defense in depth. We can restrict permissions at each layer. Presentation layer can only access business, business can only access data (and send response one layer down), data access layer can only send responses to business layer.
	- DMZ (Demilitarized Zone) Architecture
- Microservices Architecture
	- Divides application into small, independent services.
	- Each service handles a specific function
	- Pros: scalable, modular, and fault-tolerant
	- Cons: increased complexity in management
	- Needs to be orchestrated, which is very very difficult.
- Serverless Architecture
	- Relies on cloud providers to manage infrastructure
	- Functions run on-demand, scaling automatically
	- Pros: cost-effective and easy to scale
	- Cons: vendor lock-in and potential latency
-  Single-Page Applications
	- Client-side rendering; only necessary data is fetched
	- We use React, Angular, Vue.js, etc.
	- Only one GET request for the page, after that it's just sending AJAX and receiving JSON. We update the data on the page.
- Progressive Web Applications (PWAs)
	- Combine web and mobile app features
	- Offline access, push notifications, etc.
	- Things like Outlook