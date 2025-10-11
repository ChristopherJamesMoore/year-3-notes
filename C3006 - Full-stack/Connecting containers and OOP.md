# Ajax
<b>Asynchronous JavaScript and XML</b>
- No need for XML
- JSON is more common
- No need for asynchrony

<b>Allows</b>
- Update web page without reloading the page
- Request data from server - after page has loaded
- Receive data from server - after page has loaded
- Send data to a server - in the background

<b>Browsers support creating XML HttpRequest object</b>
- Allow JS to make a server query without loading a new page
- Can get access to HTTP response in code

<h1><font color="blue">Ajax - XMLHttpRequest object</h1></font>
<b>Sending an Ajax request</b>
- Method: GET/ POST
- URL: server file path
- async: true/ false
	- Fire off request then the client continues processing as it fires off the request, incremental load

<i>Methods</i>
- Open
	- Prepares the request for sending
- Send
	- Send the request

<b>Receiving a response</b>
- Ready state
	- 0: request not initialised
	- 1: server connection established
	- 2: request received
	- 3: processing request
	- 4: request finished and response ready
- HTTP - response status codes
	- 0: timeout
	- 200: OK
	- 404: page not found
	- 500: internal server error

<h3>Ajax syntax</h3>
<i>main.js</i>
````

````
1. Initialise new XMLHttpRequest object
2. Create event handler callback function
3. Send the request
