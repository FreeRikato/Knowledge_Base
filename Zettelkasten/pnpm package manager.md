> pnpm is a fast, disk space-efficient package manager for JavaScript. 

- pnpm is said to use an unique approach by storing packages in a global store on the machine and creating symlinks to the project directories that require them.
- [!] Also, it is necessary to understand [[production vs development vs build in nodejs]]

1. Why use pnpm? 
  - Refer [[Package managers for JS & TS]]

2. How does pnpm work?
  - npm installs packages directly into each project's `node_modules` folder
  - pnpm stores packages in a global store and creates hard links to the project directories.
  - Hence, different projects share the same package versions without duplication, optimizing disk usage

3. How to work with pnpm?
  - `pnpm add <package-name>`: installs the package as a production dependency
  - `pnpm add -D <package-name>`: installs the package as a development dependency
  - `pnpm add -O <package-name>`: installs the package as an optional dependency
  - `pnpm install`: install all dependencies listed in the `package.json` file
  - `pnpm remove (-P-D/-O)`: remove the package

