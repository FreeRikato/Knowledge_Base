 **Core idea:**
 - Determines how to respond to different incoming HTTP requests
 - Maps incoming requests (like a user clicking a link or submitting a form) to the appropriate server-side functionality.
 - Define routes -> Associate with specific URL patterns & HTTP methods -> Provide functions (route handlers) -> Executed when matching requests arrive

### HTTP Methods:
1. **Get:** Retrieves information from the server (e.g. Loads a page)
2. **Post:** Submits data to the server for processing (e.g. form submission)
3. **Put:** Updates an existing resource on the server
4. **Delete:** Removes a resource from the user

### URL Patterns:
1. Exact paths: `/about`, `/contact`
2. Paths with parameters: `/product/:productId` - to get a specific product
3. Paths with regular expression: style patterns (for advance matching)

### Route Handlers:
- Functions that execute when a matching route is found
- Receive the request (req) and response (res) objects
- Inside handler, request information (parameters, body, headers) are accessible and craft appropriate response to send back to the user

![[Routing anlogy.png]]