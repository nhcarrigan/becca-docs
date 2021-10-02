# Run Your Version of Becca

The next step is to invite your instance of Becca to your server. You can use the Discord Developer portal to generate an invitation link, or you can use the Client ID from your Becca's application page to create a link yourself. If you wish to manually create the link, the format is:

`https://discord.com/oauth2/authorize?client_id=CLIENT_ID_HERE&scope=bot`

Regardless of which method you choose, the link will open a new window allowing you to choose which server you'd like to add Becca to.

Once you have added her to your server, switch back to your terminal and run the command npm start. If you have set the `WH_URL` in your environment appropriately, Becca should send a message indicating it is online. Otherwise, you should see the text Activate the Omega! in your terminal, indicating she is online! Now you can try some of the commands to see if she is functioning correctly.

## Host a Live Version of Becca

By now you should have a successfully running local instance of Becca. Keeping this alive means you cannot shut down your computer. As an alternative, you might want to use a hosting service to run your live instance. We use DigitalOcean for our version, but there are other options. Be sure to read the documentation for your chosen platform!

If you would like to add Becca to your server, you are welcome to [invite her to your server](http://invite.beccalyria.com).
