# Contribution 

If you want to contribute, pull the branch `mindboost-dev` and create a new branch from it. You are free to push the branch up to have a personal backup from your contributions.

we recommed three types of branches:

**Personal Branch**
This branches are used to experiment for your own on a specific task but always have a personal backup
Path Styling: `/yourname/task-or-feature-name`

**Tooling branches**
This branches are used to add team wide tooling features like eslint for better coding experience
Path Styling `/tooling/tool-beeing-applied`

**Feature branches**
This branches are used to develop features for the app
Path Styling `/feature/name-of-the-branch`

## Merging branches
The recommended way to merge is a pull request on the `mindboost-dev` branch. This requires that eslint is free of issues and the application compiles successfully

Please commit all your changes in that branch and merge it (after another pull) into `mindboost-dev` and push it. So everybody is up to date and we have no issues integrating different versions. 

# Logging

This project used pino for logging on client and server side. Currently only client side is tested. 

## How to use: 
In pages and components, that are running in the client, you should use for Logging `this.$logger`

this.$logger.trace("Trace or Trance")
this.$logger.error("This is an error")
this.$logger.debug("This is a debugging log.")
this.$logger.info("This is a info log.")
this.$logger.warn("This is a warning log.")
this.$logger.fatal({...data, level: 'fatal'})

Please use this especially in catch blocks. It used pino as framework and can also provide logging.

## Setup

If you don't use Node 19 or lower than you need to work around with the node version manager. 

install node version mananger, register it with that code in your terminal.

```sh
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

Make sure you install node 19 and then run nvm use 19 before you continue. 

```bash
nvm install 19
````
```bash
nvm use 19
````

Make sure to install the dependencies:

```bash
# yarn
yarn install

# npm
npm install

# pnpm
pnpm install --shamefully-hoist
```

## Development Server

Start the development server on window.location.origin + 

```bash
npm run dev
```

## Production

Build the application for production:

```bash
npm run build
```

Locally preview production build:

```bash
npm run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
