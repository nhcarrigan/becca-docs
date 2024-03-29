# Manual Commands

Becca's primary command system has been migrated to use Discord's new slash interface. To bring up the command menu, type `/`. You can then see available commands for each bot in your server, as well as the built-in Discord features.

## Automod Commands

The `/automod` commands are used to manage Becca's automatic moderation system.

See the [automod configuration section](/configure-server.md#automod-settings) for more information.

## Becca Commands

The `/becca` commands relate to information about Becca herself.

| Command         | Parameters         | Description                                                                                                                      |
| --------------- | ------------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| `about`         | `null`             | Returns details about Becca's bot instance.                                                                                      |
| `adventure`     | `null`             | Returns an image from one of Becca's adventures.                                                                                 |
| `announcements` | `channel: Channel` | Sets your `channel` to follow our server's announcement channel. You will automatically get our announcements in your `channel`. |
| `art`           | `null`             | Returns an art sample from Becca's gallery.                                                                                      |
| `contact`       | `null`             | Provides links to contact the development team.                                                                                  |
| `donate`        | `null`             | Returns information on donating to support Becca's development.                                                                  |
| `emote`         | `null`             | Provides a random Becca emote.                                                                                                   |
| `feedback`      | `null`             | Provides a link to our feedback site.                                                                                            |
| `help`          | `null`             | Provides a series of links explaining how to use Becca.                                                                          |
| `invite`        | `null`             | Provides a link to invite Becca to a server.                                                                                     |
| `ping`          | `null`             | Returns Becca's response time to commands, the websocket latency, and the database ping.                                         |
| `privacy`       | `null`             | Returns a link to Becca's privacy policy.                                                                                        |
| `profile`       | `null`             | Returns a link to Becca's profile page.                                                                                          |
| `stats`         | `view: Stat`       | Provides a leaderboard for the chosen `view`                                                                                     |
| `translators`   | `null`             | Lists the wonderful folks who have helped translate Becca.                                                                       |
| `updates`       | `null`             | Displays the latest changes in Becca's code and the link to the change log.                                                      |
| `uptime`        | `null`             | Returns the time since Becca came online.                                                                                        |

## Code Commands

The `/code` commands contain tools that may be helpful to developers.

| Command   | Parameters        | Description                                                                                            |
| --------- | ----------------- | ------------------------------------------------------------------------------------------------------ |
| `caniuse` | `feature: string` | Provides a breakdown of browser support for the given `feature`.                                       |
| `colour`  | `hex: string`     | Generates an embed depicting the given `hex` colour. `hex` must be a valid 6-digit hexadecimal string. |
| `http`    | `status: number`  | Returns a cute cat image depicting the given `status` code.                                            |

## Community Commands

The `/community` commands offer a variety of tools for engaging with your community.

| Command       | Parameters                                                                                                                         | Description                                                                                                                                                                                                                                         |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `leaderboard` | `null`                                                                                                                             | Returns the server's leaderboard, provided the level system is enabled.                                                                                                                                                                             |
| `level`       | `user?: User`                                                                                                                      | Returns your current level information, or the `user`'s level information.                                                                                                                                                                          |
| `motivation`  | `null`                                                                                                                             | Gives a motivational quote.                                                                                                                                                                                                                         |
| `poll`        | `duration: number`, `unit: string`, `question: string`, `optionA: string`, `optionB: string`, `optionC: string`, `optionD: string` | Creates an embed with the question and four options. Adds buttons which users can click to vote for an option. Closes the poll when someone tries to vote after `duration` `units` have passed, and displays the results. Users can only vote once. |
| `schedule`    | `time: number`, `channel: noVoiceChannel`, `message: string`                                                                       | Provided you have permission to do so, schedules your `message` to be sent in the `channel` after `time` minutes have passed.                                                                                                                       |
| `server`      | `null`                                                                                                                             | Returns detailed information about the current Discord server.                                                                                                                                                                                      |
| `star`        | `user: User`, `reason: string`                                                                                                     | Gives the `user` a shiny gold star for the given `reason`.                                                                                                                                                                                          |
| `starcount`   | `null`                                                                                                                             | Generates an embed with the top ten users by number of stars received, and notes your rank on that leaderboard.                                                                                                                                     |
| `suggest`     | `suggestion: string`                                                                                                               | If the server has set up a suggestion channel, generates an embed in that channel with your `suggestion`. Adds reactions for members to vote on the suggestion.                                                                                     |
| `ticket`      | `reason: string`                                                                                                                   | If the ticket system is configured, creates a new ticket for the given `reason`.                                                                                                                                                                    |
| `topic`       | `null`                                                                                                                             | Provides a random conversation starter.                                                                                                                                                                                                             |
| `userinfo`    | `user?: User`                                                                                                                      | Returns basic information on the `user`'s (or your) Discord account.                                                                                                                                                                                |

## Config Commands

The `/config` commands are used to manage the [server settings](/configure-server.md). These require the `Manage Server` permission to use. Refer to that page for the valid settings and parameters.

See the [configuration section](/configure-server.md#global-configurations) for more information.

## Emote Commands

The `/emote` commands allow you to perform an emote action on another user. The emotes a user has received is tracked.

| Command | Parameters                     | Description                                  |
| ------- | ------------------------------ | -------------------------------------------- |
| `use`   | `emote: Choices`, `user: User` | Uses the chosen `emote` on the given `user`. |
| `view`  | `null`                         | Shows a count of the emotes you've received. |

## Games Commands

The `/games` commands are fun and silly commands to add a bit of charm to your community.

| Command    | Parameters        | Description                                                                                                                                         |
| ---------- | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `fact`     | `null`            | Returns a random fun fact.                                                                                                                          |
| `habitica` | `id: Habitica ID` | Returns information on the provided user's Habitica progress. Note that `id` is the user's ID (available in their profile URL), NOT their username. |
| `joke`     | `null`            | Returns a random joke.                                                                                                                              |
| `quote`    | `null`            | Returns a random quote.                                                                                                                             |
| `mtg`      | `card: string`    | Fetches and displays information on the given Magic: The Gathering `card`.                                                                          |
| `slime`    | `null`            | Gives you a random slime-themed nickname.                                                                                                           |
| `sus`      | `null`            | Selects an Among Us colour and declares it sus!                                                                                                     |
| `trivia`   | `null`            | Stars a trivia game. Players will have 30 seconds to select an answer using the buttons. At the end of the timer, Becca will announce the winners.  |

## Level Commands

The `/levels` commands manage Becca's levelling system, which rewards users for activity.

See the [level configuration section](/configure-server.md#level-settings) for more information.

## Log Commands

The `/log` commands manage Becca's logging system, which tracks specific Discord events.

See the [log configuration section](/configure-server.md#log-settings) for more information.

## Manage Commands

The `/manage` commands help with managing your community.

| Command      | Parameters                                                  | Description                                                                                                                      |
| ------------ | ----------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| `resetlevel` | `null`                                                      | Resets the level leaderboard, clearing all data.                                                                                 |
| `resetstars` | `null`                                                      | Resets the star counts, clearing all data.                                                                                       |
| `suggestion` | `action: approve \| deny`, `id: string`, `reason: string`   | Updates the suggestion embed with the given message `id`, marking it with the `action` and stating the `reason` for that action. |
| `xpmodify`   | `action: add \| remove`, `user: User`, `adjustment: number` | Either `add` or `remove` the specified `adjustment` to the XP of the given `user`.                                               |

## Misc Commands

The `/misc` commands are things that did not fit in to any other category.

| Command       | Parameters        | Description                                                                                            |
| ------------- | ----------------- | ------------------------------------------------------------------------------------------------------ |
| `echo`        | `input: string`   | Posts the given `input` as a message from Becca.                                                       |
| `orbit`       | `null`            | Returns the Orbit leaderboard for our community, and links to join the community.                      |
| `permissions` | `null`            | Confirms that Becca has the correct permissions in the server and in the channel this command is used. |
| `space`       | `date?: string`   | Returns the NASA Astronomy Photo of the Day, either from today or `date` (formatted as `YYYY-MM-DD`).  |
| `username`    | `length?: number` | Generates a DigitalOcean themed username with a max length of `number` or 30.                          |
| `xkcd`        | `number?: number` | Returns the latest XKCD comic, or the comic matching `number`.                                         |

## Moderation Commands

The `/mod` commands provide tools for moderating your community. These will all log to your moderation log channel. When a user is the target of a moderation action, Becca will attempt to DM them to notify them of the action, with the `reason` that is provided.

The audit log entry will include the moderator who performed the action and the reason provided.

> [!NOTE]
> If the target `user` also has the requisite permissions to use the command, the command will not work on them.

| Command   | Parameters                                                         | Description                                                                                                          |
| --------- | ------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------- |
| `ban`     | `user: User`, `reason: string`                                     | Bans the `user` from the server for the given `reason`.                                                              |
| `kick`    | `user: User`, `reason: string`                                     | Kicks the `user` fromt he server for the given `reason`.                                                             |
| `history` | `user: User`                                                       | Shows an embed with the number of each action that the `user` has received.                                          |
| `mute`    | `user: User`, `duration: number`, `unit: string`, `reason: string` | Issues a Discord timeout to the `user` for the given `duration` in `unit`s (i.e. 3 days), for the provided `reason`. |
| `unban`   | `user: User`, `reason: string`                                     | Unbans the `user` from the server for the given `reason`.                                                            |
| `unmute`  | `user: User`, `reason: string`                                     | Removes the Discord timeout on the `user` for the given `reason`.                                                    |
| `warn`    | `user: User`, `reason: string`                                     | Issues a warning to the `user` for the given `reason`, and adds that warning to their record.                        |

## OptOut Commands

The `/optout` command allows you to opt out (or back in) to features that require data collection. This command has no subcommands.

## Post Commands

The `/post` commnads allow you and your team to manage a post through Becca. This is great for things like a rules post. Note that `delete` and `edit` only work for posts that Becca created.

| Command  | Parameters                | Description                                                            |
| -------- | ------------------------- | ---------------------------------------------------------------------- |
| `create` | `channel: noVoiceChannel` | Uses a modal to help you create a new post in the specified `channel`. |
| `delete` | `link: string`            | Fetches the message at the `link` and deletes it.                      |
| `edit`   | `link: string`            | Fetches the message at the `link` and allows you to edit it.           |

## Reaction Role Commands

The `/reactionrole` system allows you to set up reaction roles, a common feature among Discord bots. Becca's approach, however, is a bit different. Rather than using emoji, Becca uses Discord's message buttons to assign roles. This allows her to offer faster and more reliable response times.

| Command  | Parameters                                                    | Description                                                                                                                                                                |
| -------- | ------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `create` | `channel: noVoiceChannel`, `header: string`, `roles: ...Role` | Creates a message in the given `channel`, using the `header` as the content. Takes up to 20 role parameters, and creates a button for each one so users can add/remove it. |

## Support Commands

The `/support` commands are related to receiving support from our team.

| Command  | Parameters   | Description                                                                                                                                    |
| -------- | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `data-request` | `null` | Returns a copy of the data we have stored about you, and the current server(if you are the owner). |
| `ids`    | `null`       | Returns a list of Discord IDs that will help our support team. You should run this in your server, and share the values in our support server. |
| `logs`   | `id: string` | Only available to our team, this command searches the debug logs for issues related to the given server `id`.                                  |
| `server` | `null`       | Provides an invite to the support server.                                                                                                      |

## Trigger Commands

The `/triggers` commands manage your server's specific triggers. These commands require permission to manage the server.

| Command  | Parameters                            | Description                         |
| -------- | ------------------------------------- | ----------------------------------- |
| `add`    | `trigger: string`, `response: string` | Adds a new trigger to your server.  |
| `remove` | `trigger: string`                     | Removes a trigger from your server. |
| `view`   | `null`                                | Shows all triggers on your server.  |

## User Config Commands

The `/userconfig` commands allow you to personalise some of Becca's features and responses. These settings are global (will work for you in any server) and tied to your user ID.

| Command     | Parameters                                                     | Description                                        |
| ----------- | -------------------------------------------------------------- | -------------------------------------------------- |
| `levelcard` | `background: string`, `foreground: string`, `progress: string` | Configures the theme for your personal level card. |
| `view`      | `null`                                                         | Lists your current settings.                       |

## Welcome Commands

The `/welcome` commands allow you to manage how Becca will greet and dismiss your users.

See the [welcome configuration section](/configure-server.md#welcome-settings) for more information.
