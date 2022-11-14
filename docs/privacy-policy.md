# Privacy Policy

The use of this application ("Becca") in a server requires the collection of some specific user data ("Data"). The Data collected includes, but is not limited to, user names, user nicknames, and Discord user ID values. Use of Becca is considered an agreement to the terms of this Policy.

## Access to Data

Access to Data is only permitted to Becca's developers, and only in the scope required for the development, testing, and implementation of features for Becca. Data is not sold, provided to, or shared with any third party, except where required by law or a Terms of Service agreement. You may request a copy of your data via [our support server](https://chat.nhcarrigan.com) or [email](mailto:privacy@beccalyria.com).

## Storage of Data

Data is stored in a MongoDB database. The database is secured to prevent external access, however no guarantee is provided and Becca's owners assume no liability for the unintentional or malicious breach of Data. In the event of an unauthorised Data access, users will be notified through the Discord client application.

## Off-Platform Data

Becca collects the following data for the following purposes. These data are stored in our database.

### Activity System

Becca tracks the number of times you use a command or component. This data is used to identify users who interact with the bot more.

- `User ID`: Becca uses your Discord user ID to identify you and associate the database record with your account.
- `Activity`: Becca tracks the number of times you have used an application command (slash command, button, context menu, select menu). Becca does not store any specific information about those commands, just the counts.

**Visibility**: This data is publicly visible through the `activity` context menu option.

**Optout**: You can opt out of this data collection with the `/optout` command, or by request in our [support server](https://chat.nhcarrigan.com). This data is not automatically deleted, but can be deleted upon request in our [support server](https://chat.nhcarrigan.com).

### Currency System

Becca tracks your total currency value and the last time you used a currency command. This data is used to manage the currency-based rewards for our support server, and for the cooldown systems on currency commands.

- `User ID`: Becca uses your Discord user ID to identify you and associate the database record with your account.
- `Currency Total`: Becca tracks your currency total.
- `Command Usage`: Becca tracks when you last used each currency command for the cooldown system.

**Visibility**: This data is not publicly visible, but will be seen by other members when you use the `/currency view` command.

**Optout**: You can opt out of this data collection by refraining from using the `/currency` commands, or by using the `/optout` command, or by request in our [support server](https://chat.nhcarrigan.com). This data is not automatically deleted, but can be deleted upon request in our [support server](https://chat.nhcarrigan.com).

### Emote System

Becca tracks the number of times you have been the target of an `/emote` command. This is used to show which users receive more hugs, for example.

- `User ID`: Becca collects your Discord user ID to identify you and associate the database record with your account.
- `User Name`: Becca stores your latest username and discriminator to render the data.
- `Emote Counts`: Becca keeps a count of the number of emotes you've received.

**Visibility**: This data is publicly visible when using an `/emote` command.

**Optout**: You can opt out of this data collection by using the `/optout` command, or by request in our [support server](https://chat.nhcarrigan.com). This data is not automatically deleted, but can be deleted upon request in our [support server](https://chat.nhcarrigan.com).

### Level System

_If enabled in the server_, Becca will track message activity. Becca does not store the message content, but looks at the length of the content as part of the experience point calculation. This data is stored to allow server members to see their level, the top 10 active members, and for server managers to provide roles and other perks based on user engagement.

- `User ID`: Becca uses your Discord user ID to identify you and associate the database record with your account.
- `User Name`: Becca stores your latest username and discriminator to construct the levels leaderboard.
- `Avatar`: Becca stores your latest avatar URL for use on the web view.
- `Experience Points`: Becca awards experience points based on your message activity. Becca does _not_ store message content or metadata.
- `Last Seen`: Becca tracks the last time you were seen sending a message in the server for the cooldown and the level command.

**Visibility**: This data is publicly visible through the `/community level` and `/community leaderboard` commands.

**Optout**: You can opt out of this data collection by using the `/optout` command, or by request in our [support server](https://chat.nhcarrigan.com). Your level data for a server is automatically deleted if you leave that server.

### Moderation History

Becca keeps a track of moderation actions taken against a user in a server. This data is used to facilitate future moderation decisions.

- `Server ID`: Becca uses the server ID to associate a record with a server.
- `User ID`: Becca uses your Discord user ID to identify you and associate the database record with your account.
- `Moderation Actions`: Becca tracks the number of times a moderation action has been applied. Becca does not track the reasons for a moderation action.

**Visibility**: This data is only visible to members of a server who have the `Kick Members`, `Moderate Members`, or `Ban Members` permission. Data from one server is not visible in another.

**Optout**: To preserve the integrity of our moderation system, this data (which does not include PII) cannot be opted out of or deleted.

### Scheduled Post System

When you use the `/community schedule` command to schedule a post, Becca will store the post information in the database until the post is sent.

- `Server ID`: Becca needs to know which server to send the post in.
- `User ID`: Becca uses your ID to ping you when the post is sent.
- `Scheduled Timestamp`: Becca tracks the timestamp when the post is scheduled to go out.
- `Channel ID`: Becca needs to know which channel to send the post in.
- `Language`: Becca uses the language setting from your server for the translatable portions of the embed.
- `Message`: Becca needs to save the message you intend to send.

**Visibility**: This data is not visible when stored, and is only visible to members who can see the channel when the post is sent.

**Optout**: To optout, refrain from using the `/community schedule` command.

### Server Configuration System

Becca stores the server ID and server name to associate a Discord server with it's configuration settings. This data is used to enable/disable/configure many of Becca's features.

- `Server ID`: Becca uses the Server ID to associate the data with your server.
- `Server Name`: Becca uses the server name for developers to investigate configuration issues.
- `Configuration`: Becca stores your server's [configuration data](configure-server.md).

**Visibility**: This data is visible through the `/config`, `/automod`, and `/log` commands _only_ for members with the `Manage Server` permission.

**Optout**: You can opt out of this data collection by removing Becca from your server. This data is automatically deleted when Becca leaves a server.

### Star System

Becca tracks the total number of stars each user has received in a server. This data is used for server members to recognise other members' contributions, and for managers to offer perks based on those contributions.

- `User ID`: Becca uses your Discord user ID to identify you and associate the database record with your account.
- `User Name`: Becca stores your latest username and discriminator to construct the star count leaderboard with.
- `Avatar`: Becca stores your latest avatar URL for use on the web view.
- `Star Total`: Becca tracks your star total.

**Visibility**: This data is publicly visible through the `/community starcount` command.

**Optout**: You can opt out of this data collection by using the `/optout` command, or by request in our [support server](https://chat.nhcarrigan.com). Your data for a specific server is automatically deleted when you leave that server.

### Usage Tracking

Becca tracks an anonymous total count of the usage of each command/subcommand. This data is used to plan future development features and deprecations.

- `Command/Subcommand`: Becca tracks the name of the command and subcommand used.
- `Uses`: Becca tracks the number of times that command/subcommand has been used.

**Visibility**: This data is publicly visible through the `/becca stats` command, as well as the [dashboard](https://dash.beccalyria.com?utm_source=docs&utm_medium=privacy-policy).

**Optout**: As this data is entirely anonymous, there is no opt-out or deletion available.

### Vote Tracking

Becca tracks the number of times a user votes for our support server or bot on top.gg. This data is used for potential perks and rewards.

- `User ID`: Becca uses your Discord user ID to identify you and to associate the data with your account.
- `Server Votes`: Becca counts the number of times you have voted for our support server on top.gg.
- `Bot Votes`: Becca counts the number of times you have voted for her on top.gg.

**Visibility**: This data is publicly visible through the `/becca stats` command.

**Optout**: You can opt out of this data collection by refraining from voting for the bot/server, or by using the `/optout` command, or by request in our [support server](https://chat.nhcarrigan.com). This data is not automatically deleted, but can be deleted upon request in our [support server](https://chat.nhcarrigan.com).

## On-Platform Data

The following data are stored _exclusively_ on Discord, and are **not** stored in our database.

### Debug Information

By inviting Becca to your Discord Server, you agree that information may be exposed to the development team via a private webhook. Such information includes, but may not be limited to:

- The Server Name and ID
- The Server Owner's Name and ID
- Information related to errors generated in the server.

**Visibility**: This data is only visible to members of the development and support team.

**Optout**: You can opt out of this data collection by removing Becca from your server.

### Moderation Logging

When you join a server that Becca is in, it is entirely possible that the server managers have enabled Becca's moderation logging. If this is enabled, then some of your data may or may not be sent to a channel on the server (specified by the server managers).

Please refer to [the log settings](configure-server.md) for more information on which data are potentially logged.

> [!WARNING]
> Becca's development team does not enforce any control over the moderation logging settings. If you wish to delete the on-platform data, you will need to work with the server managers and/or Discord. Additionally, you may only opt out of this data logging by leaving the server.

### Feedback System

When you submit feedback through the `/becca feedback` command, the following information is posted in an embed in our support server:

- The feedback you share.
- Your user tag and avatar.
- The name of the server you used the command in.

**Visibility**: This data is visible to members of our support server.

**Optout**: You can opt out of this by not using the `/becca feedback` command. You can also join the support server to request previously sent feedback be removed.

## User Rights

At any time, you have the right to request to view the Data pertaining to your Discord account. You may submit a request through the Discord server. You have the right to request the removal of relevant Data.

## Underage Users

The use of Becca is not permitted for minors under the age of 13, or under the age of legal consent for their country. This is in compliance with the Discord Terms of Service. No information will be knowingly stored from an underage user. If it is found out that a user is underage we will take all necessary action to delete the stored data.

## Questions

If you have any questions or are concerned about what data might be being stored from your account you may join our [support server](https://chat.nhcarrigan.com) or [email us](mailto:privacy@beccalyria.com). For more information check the Discord Terms Of Service.
