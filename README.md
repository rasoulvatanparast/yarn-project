# Yarn Starter Project

It's a Yarn Starter Project to get familiar with the Yarn

## Why Yarn

Seems like Yarn is faster to download Dependencies in IRAN :/

## Configuration Globally

Installing Yarn globally

```bash
$ sudo npm install -g yarn
```

If you want to figure out which version you installed type this following command in Terminal:

```bash
$ yarn --version
```
```bash
Output
1.22.21
```

## Creating a NodeJs Project with Yarn

Create a folder and navigate to created folder

```bash
$ mkdir first-yarn-project
$ cd first-yarn-project
```

Now use this following command to set version to `berry`.

It will create a package.json file within the directory.

```bash
$ yarn set version berry
```

```bash
Output
➤ YN0000: Done in 0s 6ms
```

The version of Yarn in the Project directory is gonna be different now, thanks to above command.

```bash
$ yarn --version
```

```bash
Output
4.0.2
```

### Initialize Yarn

```bash
$ yarn init
```

```bash
Output
➤ YN0000: · Yarn 4.0.2
➤ YN0000: ┌ Resolution step
➤ YN0000: └ Completed
➤ YN0000: ┌ Fetch step
➤ YN0000: └ Completed
➤ YN0000: ┌ Link step
➤ YN0000: └ Completed
➤ YN0000: · Done in 0s 118ms
```

This command will create the below files and creates directory called `.yarn`, creates a `git` version control system and updates `package.json`

```bash
.editorconfig
.gitattributes
.gitignore
.pnp.cjs
README.md
yarn.lock
```

### Existing YARN Project

If you downloaded a yarn project e.g. on github use this following command to Install dependencies and your good to go.

```bash
$ yarn install
```

### Adding New Dependency

For example we want to add Express

```bash
$ yarn add express
```

```bash
Output
➤ YN0000: · Yarn 4.0.2
➤ YN0000: ┌ Resolution step
➤ YN0085: │ + express@npm:4.18.2, accepts@npm:1.3.8, array-flatten@npm:1.1.1, body-parser@npm:1.20.1, and 58 more.
➤ YN0000: └ Completed in 2s 82ms
➤ YN0000: ┌ Fetch step
➤ YN0000: └ Completed
➤ YN0000: ┌ Link step
➤ YN0000: └ Completed
➤ YN0000: · Done in 2s 318ms
```

## Deploy a Simple Express Project Using YARN

After all that process we saw, It's the time to config a express project with typescript.

Install the following dependencies:

```bash
$ yarn add express
```

```bash
$ yarn add typescript ts-node nodemon -D
$ yarn add @types/express @types/node -D
```

add the following scripts to `package.json` to be able to run the project

```bash
"scripts": {
    "build": "tsc --project ./",
    "start:dev": "nodemon src/server.ts",
    "start:prod": "node dist/server.js"
  },
```

Overall your `package.json` should be like this, If there is any changes go ahead and change it.

Note that the versions of dependencies may be different.

```bash
{
  "name": "first-yarn-project",
  "packageManager": "yarn@4.0.2",
  "version": "1.0.0",
  "main": "server.js",
  "license": "MIT",
  "scripts": {
    "build": "tsc --project ./",
    "start:dev": "nodemon src/server.ts",
    "start:prod": "node dist/server.js"
  },
  "dependencies": {
    "express": "^4.18.2"
  },
  "devDependencies": {
    "@types/express": "^4.17.21",
    "@types/node": "^20.10.4",
    "nodemon": "^3.0.2",
    "ts-node": "^10.9.2",
    "typescript": "^5.3.3"
  }
}
```

## License

This project is licensed under the terms of the
[MIT license](/LICENSE).
