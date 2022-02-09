# Manual Commands

Becca's primary command system has been migrated to use Discord's new slash interface. To bring up the command menu, type `/`. You can then see available commands for each bot in your server, as well as the built-in Discord features.

## Automod Commands

The `/automod` commands are used to manage Becca's automatic moderation system.

| Command  | Parameters                          | Description                                        |
| -------- | ----------------------------------- | -------------------------------------------------- |
| `reset`  | `setting: Setting`                  | Resets the specified setting to its default value. |
| `set`    | `setting: Setting, value: Value`    | Sets the specified setting to the specified value. |
| `toggle` | `feature: Setting, enabled: on/off` | Toggles the automod feature on or off..            |
| `view`   | `setting: Setting`                  | Views the current value of the specified setting.  |

## Becca Commands

The `/becca` commands relate to information about Becca herself.

| Command       | Parameters   | Description                                                                                                  |
| ------------- | ------------ | ------------------------------------------------------------------------------------------------------------ |
| `about`       | `null`       | Returns details about Becca's bot instance.                                                                  |
| `adventure`   | `null`       | Returns an image from one of Becca's adventures.                                                             |
| `art`         | `null`       | Returns an art sample from Becca's gallery.                                                                  |
| `contact`     | `null`       | Provides links to contact the development team.                                                              |
| `donate`      | `null`       | Returns information on donating to support Becca's development.                                              |
| `emote`       | `null`       | Provides a random Becca emote.                                                                               |
| `help`        | `null`       | Provides a series of links explaining how to use Becca.                                                      |
| `invite`      | `null`       | Provides a link to invite Becca to a server.                                                                 |
| `ping`        | `null`       | Returns Becca's response time to commands, the websocket latency, and the database ping.                     |
| `privacy`     | `null`       | Returns a link to Becca's privacy policy.                                                                    |
| `profile`     | `null`       | Returns a link to Becca's profile page.                                                                      |
| `stats`       | `view: Stat` | Provides a leaderboard for the chosen `view`                                                                 |
| `translators` | `null`       | Lists the wonderful folks who have helped translate Becca.                                                   |
| `updates`     | `null`       | Displays the latest changes in Becca's code, the next expected release date, and the link to the change log. |
| `uptime`      | `null`       | Returns the time since Becca came online.                                                                    |

## Code Commands

The `/code` commands contain tools that may be helpful to developers.

| Command   | Parameters        | Description                                                                                            |
| --------- | ----------------- | ------------------------------------------------------------------------------------------------------ |
| `caniuse` | `feature: string` | Provides a breakdown of browser support for the given `feature`.                                       |
| `colour`  | `hex: string`     | Generates an embed depicting the given `hex` colour. `hex` must be a valid 6-digit hexadecimal string. |
| `http`    | `status: number`  | Returns a cute cat image depicting the given `status` code.                                            |

## Community Commands

The `/community` commands offer a variety of tools for engaging with your community.

| Command       | Parameters                                                                                     | Description                                                                                                                                                                                         |
| ------------- | ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `leaderboard` | `null`                                                                                         | Returns the server's leaderboard, provided the level system is enabled.                                                                                                                             |
| `level`       | `user?: User`                                                                                  | Returns your current level information, or the `user`'s level information.                                                                                                                          |
| `motivation`  | `null`                                                                                         | Gives a motivational quote.                                                                                                                                                                         |
| `poll`        | `question: string`, `optionA: string`, `optionB: string`, `optionC: string`, `optionD: string` | Creates an embed with the question and four options. Adds buttons which users can click to vote for an option. Closes the poll after 30 minutes and displays the results. Users can only vote once. |
| `role`        | `role?: Role`                                                                                  | If `role` is provided, and is configured as self-assignable, adds/removes the role from you. If not provided, returns a list of self-assignable roles.                                              |
| `schedule`    | `time: number`, `channel: Channel`, `message: string`                                          | Provided you have permission to do so, schedules your `message` to be sent in the `channel` after `time` minutes have passed.                                                                       |
| `server`      | `null`                                                                                         | Returns detailed information about the current Discord server.                                                                                                                                      |
| `star`        | `user: User`, `reason: string`                                                                 | Gives the `user` a shiny gold star for the given `reason`.                                                                                                                                          |
| `starcount`   | `null`                                                                                         | Generates an embed with the top ten users by number of stars received, and notes your rank on that leaderboard.                                                                                     |
| `suggest`     | `suggestion: string`                                                                           | If the server has set up a suggestion channel, generates an embed in that channel with your `suggestion`. Adds reactions for members to vote on the suggestion.                                     |
| `topic`       | `null`                                                                                         | Provides a random conversation starter.                                                                                                                                                             |
| `userinfo`    | `user?: User`                                                                                  | Returns basic information on the `user`'s (or your) Discord account.                                                                                                                                |

## Config Commands

The `/config` commands are used to manage the [server settings](/configure-server.md). These require the `Manage Server` permission to use. Refer to that page for the valid settings and parameters.

| Command | Parameters                          | Description                                           |
| ------- | ----------------------------------- | ----------------------------------------------------- |
| `reset` | `setting: Setting`                  | Resets the `setting` to the default value.            |
| `set`   | `setting: Setting`, `value: string` | Sets the `setting` to the provided `value`, if valid. |
| `view`  | `setting: Setting`                  | Shows the current values for the `setting`.           |

## Currency Commands

The `/currency` commands are used to earn [BeccaCoin](/currency.md), which can be exchanged for rewards in our [support server](https://links.nhcarrigan.com/discord).

| Command  | Parameters       | Description                                                                                                         |
| -------- | ---------------- | ------------------------------------------------------------------------------------------------------------------- |
| `21`     | `wager: number`  | Play a game of 21 against Becca. If you win, you get your `wager` in BeccaCoin. If you lose, you lose your `wager`. |
| `about`  | `null`           | Provides information about the currency system.                                                                     |
| `claim`  | `reward: string` | Exchanges your earned BeccaCoin for a given reward.                                                                 |
| `daily`  | `null`           | Generates your daily currency reward.                                                                               |
| `slots`  | `wager: number`  | Play a game of slots for double or nothing on your `wager`.                                                         |
| `weekly` | `null`           | Generates your weekly currency reward.                                                                              |

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
| `mtg`      | `card: string`    | Fetches and displays information on the given Magic: The Gathering `card`.                                                                          |
| `slime`    | `null`            | Gives you a random slime-themed nickname.                                                                                                           |
| `sus`      | `null`            | Selects an Among Us colour and declares it sus!                                                                                                     |
| `trivia`   | `null`            | Stars a trivia game. Players will have 30 seconds to select an answer using the buttons. At the end of the timer, Becca will announce the winners.  |

## Log Commands

The `/log` commands manage Becca's logging system, which tracks specific Discord events.

| Command | Parameters                          | Description                                           |
| ------- | ----------------------------------- | ----------------------------------------------------- |
| `reset` | `setting: Setting`                  | Resets the `setting` to the default value.            |
| `set`   | `setting: Setting`, `value: string` | Sets the `setting` to the provided `value`, if valid. |
| `view`  | `null`                              | Shows the current values for all settings.            |

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
| `orbit`       | `null`            | Returns the Orbit leaderboard for our community, and links to join the community.                      |
| `permissions` | `null`            | Confirms that Becca has the correct permissions in the server and in the channel this command is used. |
| `space`       | `date?: string`   | Returns the NASA Astronomy Photo of the Day, either from today or `date` (formatted as `YYYY-MM-DD`).  |
| `username`    | `length?: number` | Generates a DigitalOcean themed username with a max length of `number` or 30.                          |
| `xkcd`        | `number?: number` | Returns the latest XKCD comic, or the comic matching `number`.                                         |

## Moderation Commands

The `/moderation` commands provide tools for moderating your community. These will all log to your moderation log channel. When a user is the target of a moderation action, Becca will attempt to DM them to notify them of the action, with the `reason` that is provided.

| Command   | Parameters                                                         | Description                                                                                                          |
| --------- | ------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------- |
| `ban`     | `user: User`, `reason: string`                                     | Bans the `user` from the server for the given `reason`.                                                              |
| `kick`    | `user: User`, `reason: string`                                     | Kicks the `user` fromt he server for the given `reason`.                                                             |
| `history` | `user: User`                                                       | Shows an embed with the number of each action that the `user` has received.                                          |
| `mute`    | `user: User`, `duration: number`, `unit: string`, `reason: string` | Issues a Discord timeout to the `user` for the given `duration` in `unit`s (i.e. 3 days), for the provided `reason`. |
| `unmute`  | `user: User`, `reason: string`                                     | Removes the Discord timeout on the `user` for the given `reason`.                                                    |
| `warn`    | `user: User`, `reason: string`                                     | Issues a warning to the `user` for the given `reason`, and adds that warning to their record.                        |

## nhcarrigan Commands

The `/nhcarrigan` commands are locked to the bot's owner ID, and are used to manage the operations of the bot.

| Command      | Parameters                     | Description                                                                                                         |
| ------------ | ------------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| `purge`      | `user: string`, `data: string` | Becca will purge all `data` data (i.e. `level` data) associated with the `user` id.                                 |
| `register`   | `null`                         | Becca will re-register all application commands. Use this when a command's `data` has been changed (not the `run`). |
| `unregister` | `command: string`              | Becca will unregister a specific command, deleting it from the list.                                                |
| `viewslash`  | `null`                         | Becca will fetch all current available commands.                                                                    |

## reactionrole Commands

The `/reactionrole` system allows you to set up reaction roles, a common feature among Discord bots. Becca's approach, however, is a bit different. Rather than using emoji, Becca uses Discord's message buttons to assign roles. This allows her to offer faster and more reliable response times.

| Command  | Parameters                                            | Description                                                                                                                                                               |
| -------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `create` | `channel: Channel`, `title: string`, `roles: ...Role` | Creates a message in the given `channel`, using the `title` as the content. Takes up to 20 role parameters, and creates a button for each one so users can add/remove it. |

## triggers Commands

The `/triggers` commands manage your server's specific triggers. These commands require permission to manage the server.

| Command  | Parameters                            | Description                         |
| -------- | ------------------------------------- | ----------------------------------- |
| `add`    | `trigger: string`, `response: string` | Adds a new trigger to your server.  |
| `remove` | `trigger: string`                     | Removes a trigger from your server. |
| `view`   | `null`                                | Shows all triggers on your server.  |
