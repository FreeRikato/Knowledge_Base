- automatic restarting of server on file change
- eliminate the need to manually stop and restart the server during development. 

> Should nodemon be installed as a development or production package?
  - Development packages since it facilitates real-time updates and testing.
  - In production, automatic restart on file change is unnecessary and could lead to unintended behaviour

- [~] How to setup nodemon for Javascript -

1. Install Nodemon as Development dependency:
```bash
pnpm add -D nodemon
```
2. Configure pacakge.json:
```json
{
  "scripts": {
    "start": "node app.js",
    "dev": "nodemon app.js"
  }
}
```
- [~] How to setup nodemon for Typescript -

1. Install Nodemon and ts-node as Development dependencies:
```bash
pnpm add -D nodemon ts-node
```
2. Configure package.json:
```json
{
  "scripts": {
    "dev": "nodemon --exec ts-node src/index.js"
  }
}
```
