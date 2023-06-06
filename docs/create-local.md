# Create a Local Instance

There are a few steps you will need in order to set up a local instance of Becca. You will need some knowledge of JavaScript, TypeScript, node, and git. If you are not comfortable with doing this, you can [join our server](http://chat.nhcarrigan.com) to meet Becca there.

## Clone the GitHub Repository

Before doing anything else, you have to make sure you have a GitHub Account. If you do not have one, we recommend [signing up for free here](https://github.com/signup).

Once you have signed in to GitHub, navigate to our [GitHub repository](https://github.com/BeccaLyria/discord-bot) and either fork the repository into your own account or download the files to your computer.

## Install the Necessary Software

> [!TIP]
> While we make our best effort to maintain a friendly developer experience across all platforms, please note that our primary environment is Ubuntu via WSL2 - some things may not work as expected in other environments.

Using your preferred development environment (if you do not have one, we recommend either Visual Studio Code (VSCode) or Atom), load the directory containing your copy of Becca's files.

Before you do anything else, make sure that Node.js and pnpm are installed. If you do not have Node.js installed, you can do so from the Node.js website. If you do not have pnpm installed, you can do so from the pnpm website. You should be running Node.js version 18.15.0 or higher, and pnpm version 8.6.1 or higher. Open the terminal - you will now need to install some packages using pnpm. Enter the following commands into the terminal to perform the installations:

`pnpm install` - This will install all of the dependencies found in the package.json file automatically. If this does not work, you will need to go through each item listed in that file and run `pnpm install [packagename]`

> [!NOTE]
> After installing the dependencies, Prisma will automatically generate the type definitions for the database client based on the schema.

`pnpm run build` - This will build the TypeScript files into runnable JavaScript files.

Congratulations! You are now ready to run the code locally - the start command is `pnpm run start`. To connect the code to your Discord Bot application, continue reading.

## Requirements

| Name      | Version | Instructions                                                                                                        |
| --------- | ------- | ------------------------------------------------------------------------------------------------------------------- |
| Node.js   | 18.15.0 | [Download](https://nodejs.org/en/download/)                                                                         |
| pnpm      | 8.6.1   | [Install](https://pnpm.io/installation)                                                                             |
| MongoDB   | 6.0.5   | [Atlas Instructions](https://www.freecodecamp.org/news/get-started-with-mongodb-atlas/)                             |
| Sentry.io | null    | [Sentry Instructions](https://www.freecodecamp.org/news/how-to-add-sentry-to-your-node-js-project-with-typescript/) |
