<h3>Full-stack developer skills</h3>
<b>Client-side</b> skills
- Markdown, Styling, JS
- jQuery
- Angular
- React JS/ TS
<b>Server-side</b> skills
- NodeJS
- ExpressJS
- ASP.Net
- Python
- Java
- PHP
<b>Database</b> skills
- MongoDB
- SQL Server
- Postgres
- Oracle
<h3>MEAN and MERN stack</b>
The MEAN stack follows a <u>model-view-controller</u>[^1] architecture, which provides a structured approach to application development. This makes it well suited for enterprise level applications and large-scale projects that projects that require strict architecture and code consistency. It uses Typescript for front-end UI which offers better tooling for large teams. MEAN is preferred for complex and large applications where a predefined structure is beneficial.

On the other hand, the MERN stack uses a <u>component-based</u>[^2] architecture with the React framework, offering amazing flexibility and modularity. Reacts virtual DOM[^3] enhances rendering performance, making it practically effective for dynamic and interactive user interfaces, such as single-page applications, dashboards, and real-time applications. MERN is often favoured for its rapid development of smaller applications and startups aiming for quick MVPs. 

[^1] Model-view-controller architectures commonly are used for developing user interfaces that <u>divides the related program logic into three interconnected elements</u>. 
These elements are:
- The model - the internal representations of information.
- The view - the interface that presents information to and accepts it from the user.
- The controller - the software linking the two.
[^2] Component-based architecture is used for developing user interfaces by <u>segmenting UI its loosely coupled and reusable components</u>. This emphasises the separation of concerns among components.
[^3] Reacts virtual DOM is an in-memory, lightweight JS representation of the actual DOM (document object model), serving as a blueprint for the user interface. It is created by React <u>whenever a component is rendered, storing a copy of the UI structure in memory</u>.

<h3>Context/ component/ container</h3>
 ![[Pasted image 20250923133815.png]]
 
A sample of full-stack architecture.

<b>Components</b>
- User facing application
- Browser
	- Sends requests to front-end server
	- Receives static files and API responses
<b>Front-end server</b>
- HTTP server
	- Serves static files (HTML, CSS, JS)
	- Can reverse proxy[^4] API requests to back-end
- Located between client and back-end server
<b>Back-end server</b>
- Webservice (NodeJS)
	- Handles application logic
	- Processes API requests from client
	- Connects to MongoDB for data
<b>Database</b>
- MongoDB
- NoSQL database
	- Stores application data
	- Communicates with back-end server
<h3>CSS rule specificity</h3>
The algorithm used by a browser to determine which CSS declaration is the most relevant to an element. The specificity is calculated based on the types of selectors used, it assigns a weight to each selector type[^5]. The weight is often represented as a triad such as a, b, and c where a represents id-like specificity, b represents class-like specificity, and c represents element-like specificity. The selectors types contribute to the specificity score; id selectors increment a by 1, class, pseudo-class, and attribute selectors increment b by 1, and element or pseudo-element selectors increment c by 1.

<h1>Containers and docker basics </h1>
Containers are isolated environments for running instances of applications. They leverage OS level virtualisation without taking as many resources or as much time as a full OS VM.
<h3>Docker compose</h3>
```
compose.yaml
```
<i>Note: <u>compose.yaml is only for local application set-up, not cloud deployments</u></i>

The compose.yaml file is a human-friendly way to orchestrate a Docker application, defining images required, ports that need to be exposed, filesystem access, what commands to be run on start-up, etc... 
- Based on image
- Map ports
- Map disk volumes, filesystem
