# Creating Your Bot Application and Connecting it to Your Instance

Once your environment is set up, you need to connect the code to a Discord Bot application. If you have not created a Discord Bot application, you will need to follow these steps:

- Log in to the [Discord Developer site](https://discord.com/developers)

- Create a new application by clicking on the "New Application" button.

- On the left, select "Bot", then create a new bot.

## Bot Settings

After creating your bot application, you'll need to enable the `Server Members Intent` option to receive the `GUILD_MEMBERS` intent. This is required for Becca's functionality, and the bot will not load if this is disabled.

Additionally, you may wish to disable the `Public Bot` option to prevent other people from being able to invite your test application.

![Intent Settings](https://cdn.nhcarrigan.com/content/discord/intents.png)

## Create a Webhook

Becca is configured to send an online notice, and updates on servers it leaves or joins, through a Discord Webhook. In your server, create a new Webhook and copy the URL.

You can refer to the [official documentation](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks) for creating a new Webhook.

You will need this Webhook URL for the next step.

It looks something like:

`https://discordapp.com/api/webhooks/ID/TOKEN`

## Link Your Bot Application to Becca's Code

> [!ATTENTION]
> All of these values should go in a file specifically named `.env`. Do not modify the `sample.env` file, do not use a name other than `.env`, or your code will not run correctly.

Now that you have a bot application, you'll need to create a file called `.env`. You can either create the file manually, or copy the `sample.env` file. This file will contain the following variables:

> [!TIP]
> It is highly recommended that you use the `sample.env` file as a starting point. While some of these values are optional, the code validation will fail if they are not present (or are empty) and will prevent the application from starting. The default values in the `sample.env` will allow the application to load correctly.

These values are necessary for the overall operation of the bot.

- `DISCORD_TOKEN` (REQUIRED) - The value of this variable will be your Token from the Discord developer page. It is VERY important that you keep this token a secret - do not upload it to GitHub or share it publicly, as this will allow anyone to access your Discord Bot application. **This token is obtained by visiting your application's Bot page on the Discord Developer portal.**

- `MONGODB` (REQUIRED) - The value of this variable will be your MongoDB authentication URI. Like the token, this needs to be kept secret to prevent unauthorised access to and modification of your database. **Your URI can be obtained per the instructions on the previous page.**

- `NODE_ENV` (REQUIRED) - This tells Becca whether she is in a development state or production state - the webhook message includes this value. Set this to `development` when working locally, and `production` if you are running your own instance.

- `WH_URL` (REQUIRED) - This is the URL for the Discord webhook. Becca will log when it goes online, connects to the database, and any time a server has an error. **This is obtained from the integrations tab of a Discord channel's settings**

- `CURRENCY_WH` (REQUIRED) - This is the URL for the Discord webhook. Becca will log any activity related to the currency system. **This is obtained from the integrations tab of a Discord channel's settings**

These values are necessary for specific commands.Using an invalid value will prevent certain commands from functioning.

- `NASA_API` (OPTIONAL) - This is the API key for the NASA API. **Obtained from [the NASA Webpage](https://api.nasa.gov/)**

- `HABITICA_KEY` (OPTIONAL) - This is the API key for Habitica. **Obtained from [the Habitica Webpage](https://habitica.com/)**

- `ORBIT_KEY` (OPTIONAL) - This is the API key for Orbit. **Obtained from [the Orbit Webpage](https://orbit.love/)**

These values are Discord values required for the slash commands.

- `OWNER_ID` (REQUIRED) - This tells Becca which Discord account is her owner. She will respond just a little differently to the owner. Leaving this blank WILL lock out some commands. **This is obtained by enabling developer mode in your Discord settings, right clicking on your avatar, and selecting Copy ID**

- `CLIENT_ID` (REQUIRED) - This tells Discord which application to attach slash commands to. It should be set to your bot's ID. **This is obtained from the Application tab of your bot's page on the Discord Developer Portal. Copy the Application ID.**

- `HOME_GUILD_ID` (REQUIRED) - If you are developing locally, you'll want to set this to your server's ID. This tells Discord where to register slash commands on the guild level. Guild commands update instantly (global commands update every hour) which makes this ideal for development testing. **This is obtained by enabling developer mode in your Discord settings, right clicking on your server avatar, and selecting Copy ID.**

These values are optional and will fall back to standard Unicode characters if not present.

- `BECCA_YES` (OPTIONAL) - This is the ID or Unicode character for the emoji Becca will react with on successful command calls.

- `BECCA_NO` (OPTIONAL) - This is the ID or Unicode character for the emoji Becca will react with on failed/errored command calls.

- `BECCA_LOVE` (OPTIONAL) - This is the ID or Unicode character for the emoji Becca will use for the hearts listener.

- `BECCA_THINK` (OPTIONAL) - This is the ID or Unicode character for the emoji Becca will react with when she is @mentioned.

This is required for the Sentry logging.

- `SENTRY_DSN` (REQUIRED) - This enables external logging through Sentry.io - you will need to set up and configure a project there. **This is obtained from the instructions on the previous page.**

These values are used for the top.gg vote tracking.

- `TOPGG_PASSWORD` - This is the password you would provide to the top.gg webhook for authentication. This can be set to any string you'd like, but if you intend to set up an actual webhook you should use a secure password.

- `VOTE_CHANNEL_ID` - This should be the ID of the channel in the `HOME_GUILD_ID` guild where Becca should send vote notifications.
