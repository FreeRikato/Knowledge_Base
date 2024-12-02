
=> Production dependencies are packages required for the application to run in a production environment. 
  - These are essential for the application's core functionality and are included when the application is deployed. 
  - They are listed under the dependencies field in the package.json file.
  - Eg: Express, Mongoose

=> Development dependencies are packages needed only during the development phase of a project. 
  - These are not required in a production environment and are used for tasks such as testing, building, or linting code. 
  - They are listed under the devDependencies field in the package.json file.
  - Eg: Mocha, ESLint

=> Build dependencies refer to tools and packages needed to compile or bundle the application code before it is deployed. 
  - These can sometimes overlap with development dependencies, as they are often used during the build process to prepare the application for production.
  - Eg: Webpack, Babel

