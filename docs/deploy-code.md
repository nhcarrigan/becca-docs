# Run Your Version of Becca

The next step is to invite your instance of Becca to your server. You can use the Discord Developer portal to generate an invitation link.

##Generating the link from dashboard in developer portal

Go to [Application](https://discord.com/developers/applications) in the Discord Developer Portal.

- Open the new application that you have created in previous step.

- Click on `OAuth2` tab in the left panel.

- In the scopes section click checkboxes with `applications.commands` (you can't run slash commands without it) and `bot`.

- In the bot permissions section click on checkboxes as stated in [set-permissions](./set-permissions.md) file.

You can then copy the invitation link from the scopes section above using the `Copy` button.
>It looks something like
> `https://discord.com/oauth2/authorize?client_id=CLIENT_ID_HERE&permissions=INTEGER_CODE_HERE&scope=applications.commands%20bot`


Enter the link in a new window and it will ask you to choose which server you'd like to add your local instance of Becca to.

Once you have added her to your server, switch back to your terminal and run the command `npm start`. If you have set the `WH_URL` in your environment appropriately, Becca should send a message indicating it is online. Otherwise, you should see the text Activate the Omega! in your terminal, indicating she is online! Now you can try some of the commands to see if she is functioning correctly.

## Host a Live Version of Becca

By now you should have a successfully running local instance of Becca. Keeping this alive means you cannot shut down your computer. As an alternative, you might want to use a hosting service to run your live instance. We use DigitalOcean for our version, but there are other options. Be sure to read the documentation for your chosen platform!

If you would like to add our Becca to your server, you are welcome to [invite her to your server](http://invite.beccalyria.com).
