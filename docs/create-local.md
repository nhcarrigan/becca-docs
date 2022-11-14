# Create a Local Instance

There are a few steps you will need in order to set up a local instance of Becca. You will need some knowledge of JavaScript, TypeScript, node, and git. If you are not comfortable with doing this, you can [join our server](http://chat.nhcarrigan.com) to meet Becca there.

## Clone the GitHub Repository

Before doing anything else, you have to make sure you have a GitHub Account. If you do not have one, we recommend [signing up for free here](https://github.com/signup).

Once you have signed in to GitHub, navigate to our [GitHub repository](https://github.com/BeccaLyria/discord-bot) and either fork the repository into your own account or download the files to your computer.

## Install the Necessary Software

> [!TIP]
> While we make our best effort to maintain a friendly developer experience across all platforms, please note that our primary environment is Ubuntu via WSL2 - some things may not work as expected in other environments.

Using your preferred development environment (if you do not have one, we recommend either Visual Studio Code (VSCode) or Atom), load the directory containing your copy of Becca's files.

Before you do anything else, make sure that Node.js and npm are installed. If you do not have Node.js and npm installed, you can do so from the Node.js website. You should be running Node.js version 16.2.0 or higher, and npm version 7.6.0 or higher. Open the terminal - you will now need to install some packages using npm. Enter the following commands into the terminal to perform the installations:

`npm install` - This will install all of the dependencies found in the package.json file automatically. If this does not work, you will need to go through each item listed in that file and run `npm install [packagename]`

`npm run build` - This will build the TypeScript files into runnable JavaScript files.

Congratulations! You are now ready to run the code locally - the start command is `npm run start`. To connect the code to your Discord Bot application, continue reading.

## Requirements

| Name      | Version | Instructions                                                                                                        |
| --------- | ------- | ------------------------------------------------------------------------------------------------------------------- |
| Node.js   | 16.9.1  | [Download](https://nodejs.org/en/download/)                                                                         |
| npm       | 7.6.0   | Comes bundled with Node - update with `npm i -g npm`                                                                |
| MongoDB   | 4.4.9   | [Atlas Instructions](https://www.freecodecamp.org/news/get-started-with-mongodb-atlas/)                             |
| Sentry.io | null    | [Sentry Instructions](https://www.freecodecamp.org/news/how-to-add-sentry-to-your-node-js-project-with-typescript/) |
