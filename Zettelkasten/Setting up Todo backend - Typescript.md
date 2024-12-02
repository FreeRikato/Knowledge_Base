This is so repeated yet confusing. I will use pnpm for the package manager and let's take mongodb as the database that I can use with docker or mongodb compass. 

- Follow up with backend notebook in warp drive creating a basic express server using typescript
- Now, connect with the mongodb database using connection string and create scheme & model - user + todo
- Specify authentication routes for the backend:
	- **Get /** - Testing the server (hello world)

	- **Get /users** - Get users data
	- **Post /users/signup** - specify signup route where i get the signup payload from req.body. Hash the password using bcrypt and then asynchronously save the data in the DB. Also, exceptional cases and type validation with zod should be included for best practices.
	- **Post /users/login** - specify login route that is the login payload from req.body. Get username details using the provided username and compare the password with the stored one that is hashed during signup with bcrypt. Then, provide signed jwt token with user id and username for token authentication. Also, exceptional cases and type validation with zod should be included for best practices.
- For the middlewares, we will be implementing userauth that gets jwt bearer token from req.headers. Verify the jwt token and provide the decoded jwt token that contains user id and username to the next middleware function.
- Specify todo routes for the backend:
	- Get /todo - Get todos of the specified user from userauth
	- Post /todo - Post a new todo with title and description
	- Update /todo/:todoid - Update an existing todo with title, description or completion
	- Delete /todo/:todoid - Delete a todo from the database
