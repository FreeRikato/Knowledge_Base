[[Middleware]]
**How it enhances functionality of requests and responses?**

| **Request**                                                                 | **Response**                                                             |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **Data Enrichment:** Fetch and attach additional data to the request object | **Post Processing:** Manipulate the response before it's sent            |
| **Preprocessing:** Handles the main request logic                           | **Fine-Grained Control:** allows for precise adjustments to the response |
| **Flow control:** Make decisions that impact how the request is handled     |                                                                          |
### Core Idea
- Express application -> a series of function calls (middlewares) that are executed in response to incoming HTTP requests 
- Each middleware function has access to the request (`req`) and response (`res`) objects, plus the ability to pass control to the next middleware function
### Middleware Analogy

![[Middleware analogy.png]]

### Middleware Architecture

![[Middleware architecture.png]]

### Benefits
- **Modularisation:** Break down application logic into smaller, reusable functions for better code organisation
- **Extensibility:** Easily introduce new functionality without modifying the core routing logic
- **Customisation:** Control flow of HTTP requests, manipulating the data and response as needed