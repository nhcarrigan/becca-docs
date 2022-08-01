# Changelog

Here you can see changes made across each version of Becca.

Becca's updates are deployed every Sunday around 8AM Pacific Time.

[Version 20](#version-20) | [Version 19](#version-19) | [Version 18](#version-18) | [Version 17](#version-17) | [Version 16](#version-16) | [Version 15](#version-15) | [Version 14](#version-14) | [Version 13](#version-13) | [Version 12](#version-12) | [Version 11](#version-11) | [Version 10](#version-10) | [Version 9](#version-9)

## Version 20

### 20.1.0

- Removed the default `hearts` values from the code.
- Added option to customise level and role messages, and change the messages from embeds to text.
- Added `/optout` command to allow for users to opt out of data collection systems, instead of having to join the server.
- Removed the server-specific command usage tracking.
- Added pagination to the leaderboard command.

### 20.0.1

- Fixed bug where tied score logic ran when player hit, now it only runs on a stand.
- Added declaration for Message Content intent, fixing issues with automod and level system.

### 20.0.0

- Updated `discord.js` to version 14, refactored code.
- Fix to initial experience logic to only run if levels are enabled.
- Hack-ban members who left server, rather than throwing an error on `/mod ban`.
- Fixed bug where a tied score locked the game in `/currency 21`.
- Temporarily deprecated the `/reactionrole add` and `/reactionrole remove` commands due to type definition issues.

## Version 19

### 19.2.0

- Added option to set initial experience level.
- Implemented indexing on production database.
- Dependency updates to enable text-in-voice support.

### 19.1.2

- Reverted the experience cooldown increase that was accidentally implemented before the level migration.

### 19.1.1

- Patched issue with updated Heptagram API endpoint.
- Removed the starboard and leaderboard endpoints to address potential privacy concerns.

### 19.1.0

- Implemented monthly vote tracking to test giving a role reward.

### 19.0.2

- Made the link detection regex less sensitive, expecting http(s) to avoid false positives.

### 19.0.1

- Updated the available currency rewards
- Increased the daily and weekly currency gain amounts
- Added a partial win rate to the slots game and increased the win amounts

### 19.0.0

- Patched an error in the new `/mod` permission system.
- Patched an error in the Heptagram anti-phish endpoint.
- Updated `/games joke` command to use Heptagram API.
- Added `/games quote` command.
- Refactored the command logic for cleaner subcommand approach and improved DX.

## Version 18

### 18.6.0

- Updated the anti-phish detection system to rely on multiple APIs, minimising the chance of false positives.
- Improved the logic in `message.react` calls, allowing us to restore custom emotes.
- Deprecated the `/community role` command and the self-assignable roles configuration setting.

### 18.5.1

- Updated the `/mod` commands such that they cannot be used against members who have the same permission to use the commands.

### 18.5.0

- Added a level card image to `/community level`.
- Added `/userconfig` commands to allow card customisation.
- Updated the `/reactionrole` system to allow editing of existing posts.

### 18.4.0

- Added UTM tracking parameters to Becca's links.
- Updated the currency rewards.
- Tweaked the member remove flow.
- Added a `topgg` owner command.

### 18.3.1

- Fixed some broken i18n strings.

### 18.3.0

- Added the Mee6 migration command.

### 18.2.0

- Added anti-phishing system.
- Added currency reminder feature.
- Migrated `/nhcarrigan` commands.
- Additional i18n fixes.

### 18.1.0

- Migrated `/reactionrole` system from reactions to buttons.
- Fixed bug with `/currency 21` buttons not functioning.

### 18.0.0

- Fixed a bug in the ban appeal logic
- Improved code block detection in the link system
- Improved link detection
- Added internationalisation infrastructure
- Moved `/reactionrole` commands out of beta
- Added `/becca translators` command

## Version 17

### 17.10.0

- Added `/becca contact` command.
- Added step to sort subcommands so they appear alphabetical in Discord's UI.
- Fixed broken link in `/becca adventure` command.
- Added ban appeal config option.
- Added timeout to automatically delete link detection message.
- Emote-only channel now works on message edits.
- Added a reaction role system, with `/reactionrole` commands.

### 17.9.0

- Updated the link detection regex to capture additional 2-letter TLDs.
- Overhauled the link detection system to ignore multi-line codeblocks (too many false positives, with the way code is written) and catch links within spoilers.
- The DM sent when a user's message is caught by the link system now includes the links that were detected.
- Enabled the bot votes leaderboard, since Becca is now on top.gg
- Updated the bookmark command to no longer send the message content, addressing a potential privacy concern.
- Updated the message edit event to generate diffs instead of sending the full message content.

### 17.8.0

- Updated the `/games habitica` command to no longer send an achievements embed if the user is not found.
- Migrated the `/mod mute` and `/mod unmute` commands to use the new Discord timeout feature.
- Removed the `/nhcarrigan list`, `/nhcarrigan serverinfo`, and `/nhcarrigan leave` commands, as these were no longer needed with Becca being verified.
- Added a step to send a DM to a user when they are the target of a moderation action.
- Added a new `/mod history` command, tracking and displaying how many moderation actions a user has received.
- Updated the `/misc permissions` command to ensure all of the latest required permissions were present.
- Added a `/becca adventure` command to return images from Becca's adventures.
- Updated the `/community leaderboard`, `/community starcounts` and `/becca stats` commands to use the new table generator.
- Added the ability for users to opt-out of the emote commands.
- Added `/becca privacy` to create another way to quickly get a link to the privacy policy.

### 17.7.0

- Added `.ly` to the link detection regex.
- Added new `/manage xpmodify` command.
- Limited `/leaderboard` server endpoint to the top 100 users.
- Updated `/becca ping` command to show websocket latency and database ping.
- Fixed issue in test assertion message.
- Added developer avatar to donation CTAs for clearer branding.

### 17.6.1

- Patched an issue in the emote-only regex.

### 17.6.0

- Added an emote-only config to lock channels to emote only.

### 17.5.0

- Added link buttons to many of Becca's embeds, improving usability especially on mobile.

### 17.4.3

- Updated the denied TLDs in the link regex.

### 17.4.2

- Moved from grafana to PM2 for logging
- Patched a bug in the `/currency weekly` command

### 17.4.1

- Patched a broken query related to the new level schema.
- Added a donation CTA to the embeds.

### 17.4.0

- Overhauled the level system to be more scalable, maintaining individual documents for each user in a guild.

### 17.3.0

- Added grafana logging to capture usage metrics

### 17.2.0

- Modified the `/triggers` commands to require the `MANAGE_SERVER` permission.
- Restored the previously deprecated `habitica` command as `/games habitica`.
- Restored the previously deprecated `orbit` command as `/misc orbit`.
- Added the `/emote` commands.
- Modified the `/community schedule` command to restrict pings, avoiding a potential exploit.
- Updated the top.gg system to send reminders every 12 hours.
- Updated the `messageEdit` event to run the sass mode, automod, and triggers listeners.
- Updated the opt out system to include recently added data tracking.
- Added new art!

### 17.1.0

- Updated sass mode and default responses to use arrays, allowing for more randomised responses
- Also added Becca emotes to those responses
- Loaded three new emotes into slots list
- Updated automod system to DM user with their message if it's deleted
- Added server endpoint and database logic to track top.gg votes
- Changed update schedule to be Sunday instead of Monday
- Added new trigger system

### 17.0.0

- Refactored the type definitions
- Added tests to assert database schemas are accurate
- Separated the logging into it's own config, allowing for more granular control over event logs
- Added an endpoint to the server to access global stats
- Migrated the link detection into a separate automod system
- Added profanity filter to the automod system
- Updated the hash generation for the `/becca updates` command to generate once on load
- Added a `/becca emote` command to return a random emote
- Merged the thanks logic into sass mode, removing the `thanks` config.

## Version 16

### 16.22.0

- Added sassy mode
- Added a command leaderboard for server activity

### 16.21.0

- Added support for nicknames in thanks listener
- Moved `/becca becca` to `/becca profile`
- Bumped the experience points grant cooldown to 5 minutes
- Added the version to `/becca updates`
- Updated the `/becca donate` embed to use buttons
- Added cleanup for member data when a member leaves a server
- Developer experience tweaks

### 16.20.2

- Tweaked link detection regex
- Added more art to the art list

### 16.20.1

- Dependency updates

### 16.20.0

- Updated link regex to use config, should make things clearer for contributors.

### 16.19.0

- Added the `updates` command.

### 16.18.3

- Fixed bug in the link detection regex causing false positives.

### 16.18.2

- Added common file extensions to link detection regex.
- Fixed bug in the link detection regex causing errors.

### 16.18.1

- Bug in poll command preventing more than one total answer.

### 16.18.0

- Released full API functionality.

### 16.17.2

- Updated the structure of the `star` and `level` data to work with the API.

### 16.17.1

- Added `cors` to the API.

### 16.17.0

- Created API endpoints.
- Added new Becca emotes to `slots` command.

### 16.16.1

- Tweaks to the `nhcarrigan` owner commands to display proper command data.

### 16.16.0

- Added configuration option to select channels the level system should ignore.

### 16.15.0

- Added the `poll` command.

### 16.14.0

- Added the `slime` command.
- Updated the `permission` command to include validation for `MANAGE_NICKNAMES` and `USE_EXTERNAL_EMOTES`.

### 16.13.0

- Added `report` context command.
- Added `report channel` configuration option.

### 16.12.1

- Fixed bug in `guess` command that allowed for negative currency balance.

### 16.12.0

- Added `guess` command.
- Added `purge` command.
- Added configuration to allow users to opt out of specific data collection.

### 16.11.0

- Added `activity` context command.
- Added delete button to `bookmark` DM to allow users to delete it.
- Added tracking for user command use.

### 16.10.0

- Added `bookmark` context command.

### 16.9.2

- Added currency logging to the `21` and `slots` commands.
- Updated `21` buttons to use Becca emotes.

### 16.9.1

- Renamed "dealer" to "Becca" in `21` command.

### 16.9.0

- Added `slots` command.
- Fixed process for registering new commands / updating existing commands.
- Added additional 2-letter TLDs to the link detection regex.

### 16.8.0

- Added currency gain on command use.

### 16.7.0

- Removed the command registration on startup.
- Added text command for emergency command reload, in case slash commands are lost/unavailable.

### 16.6.3

- Added YouTube short link TLD to link detection regex.
- Added file extensions to exclude from link detection regex.

### 16.6.1

- Added file extension to exclude from link detection regex.
- Added logging for `nhcarrigan` commands
- Added choices for the `register` and `unregister` commands.

### 16.6.0

- Added new `nhcarrigan` commands to handle sending slash command data to Discord.
- Added `levelscale` command to display level scale.

### 16.4.1

- Updated link detection regex to be cleaner

### 16.4.0

- Allow file extensions to be excluded from link detection regex.

### 16.3.0

- Added anonymous tracking for global command usage.

### 16.2.0

- Added `about` command for currency system.
- Tweaked the wording for the rewards.

### 16.1.0

- Added new currency system!
- Fixed logic order for level system - don't send notification until after data is saved.

### 16.0.1

- Fixed logic order for level system.

### 16.0.0

- Complete migration to slash commands. Text commands deprecated.

## Version 15

### 15.13.0

- Slash command migration wave

### 15.12.0

- Slash command migration wave

### 15.11.1

- Slash command migration wave

### 15.11.0

- Slash command migration wave
- Deprecated `guess` command

### 15.10.0

- Slash command migration wave

### 15.9.1

- Slash command migration wave

### 15.9.0

- Becca's first slash command!

### 15.8.0

- Added the `topic` command.

### 15.7.0

- Added the `schedule` command.

### 15.6.0

- Added a configuration option for a custom message when a member leaves the server.

### 15.5.0

- Changed the link detection message to an embed.

### 15.4.0

- Changed the level up message to an embed.

### 15.3.0

- Added a config to assign a role when a member joins the server.

### 15.2.0

- Added an argument to view another user's level.

### 15.1.2

- Modified the link detection regex to not detect 2-letter TLDs.

### 15.1.1

- Patch discord.js version

### 15.1.0

- Removed encryption module from database, migrated data.

### 15.0.2

- Added logic to handle multiple links in a message.

### 15.0.1

- Improved voice channel event logging to avoid duplicate events.

### 15.0.0

- Updated to discord.js version 13.
- Added voice channel event logging.
- Added support for thread channels. Becca will join new threads automatically.
- Added thread channel event logging.

## Version 14

### 14.7.2

- Added new artwork.

### 14.7.1

- Added new player colours to `sus` command.

### 14.7.0

- Added config to allow for specific roles to be assigned at specific levels.
- Improved the logic for rendering config settings.

### 14.6.1

- Updated display of user info.

### 14.6.0

- Added config to accept allowed link regex patterns.

### 14.5.0

- Added anti-link detection system.

### 14.4.0

- _no changes_

### 14.3.1

- Added error logging system.

### 14.3.0

- Expanded information displayed in `userinfo` and `server` commands.
- Updated display embed for `permissioncheck` command.

### 14.2.0

- Added `permissioncheck` command.

### 14.1.1

- Updated ports used in monitoring endpoint to work with NGINX.

### 14.1.0

- Added config to set separate channel for levelup messages.

### 14.0.4

- Fixed message on `GUILD_DELETE` event.

### 14.0.3

- Improved logic in `list` command for rendering server owner data.

### 14.0.2

- Fixed input issues in `role` command and `config` command.

### 14.0.1

- Updated message deletion embed to display username instead of id.

### 14.0.0

- Complete refactor of Becca's logic and infrastructure to improve runtime and allow for better scalability.

## Version 13

### 13.3.2

- Updated moderation log embeds to include user ID.

### 13.3.1

- Removed the `up` reaction on messages that triggered experience gain.

### 13.3.0

- Updated moderation log embeds.
- Added tracking for warning counts.
- Updated embeds to add the author field.

### 13.2.0

- Updated `orbit` embed to include the user's score.

### 13.1.1

- Added new `sus` colours.

### 13.1.0

- Removed the role list from the `server` embed.
- Tweaked the wording of the `role` command.

### 13.0.0

- Fixed logic of moderation commands to handle failed DM notices.
- Refactored command responses to reflect Becca's personality.
- Deprecated `emote` commands.
- Refactored commands to no longer use `message.reply()`.

## Version 12

### 12.8.1

- Improved error logging to provide call stack and error message

### 12.8.0

- Added `suggestion` command.

### 12.7.1

- Patched rendering issue in config hearts embed.

### 12.7.0

- Refactored the config logic

### 12.6.0

- Added `colour` command.

### 12.5.2

- Restricted the `list` command to bot owner.
- Updated `restrict` command to log target's roles before removing.

### 12.5.1

- Added error handler to `resetStar` command.

### 12.5.0

- Added `resetStar` command.

### 12.4.0

- Added `orbit` command.

### 12.3.4

- Tweaked ban logic to send DM before banning.

### 12.3.3

- Patched `role` command to show list if no argument is provided.

### 12.3.2

- Modified `level` and `leaderboard` to use nickname instead of username, when relevant.

### 12.3.1

- Added logic to delete command call on `suggestion` success.
- Removed the success reaction from `close` command.
- Updated `becca` command to point to profile site.

### 12.3.0

- Added `levelscale` command.

### 12.2.3

- Added `up` reaction on messages which generate experience.

### 12.2.2

- Reduced level scale from 1000 to 100.

### 12.2.1

- Added logic to dynamically generate level scale.
- Added current experience points to `leaderboard` embed.
- Added bonus to experience gain based on message length.

### 12.2.0

- Implemented new sliding scale for levels.
- Added a maximum level cap.

### 12.1.1

- Fixed rendering issue in error handler.

### 12.1.0

- Added a rate limit to the level listener, restricting experience gain to once per minute.

### 12.0.0

- Added Sentry for better error logging.
- Updated all commands to use a new error handler.

## Version 11

### 11.4.1

- Added logic to prevent experience gain on command use.

### 11.4.0

- Deprecated commands that relied on `noops` API.

### 11.3.4

- Added error handling to log channel message handler.

### 11.3.3

- Fixed the letsencrypt domain in the http monitoring endpoint.

### 11.3.2

- Fixed environment error in the http monitoring endpoint.

### 11.3.1

- Fixed error in the http monitoring endpoint port.

### 11.3.0

- Added a simple HTTP endpoint for uptime monitoring.
- Fixed logic error in the `suggest` command to handle invalid suggestion channel configs.

### 11.2.1

- Patched logic error in the channel validation for the `suggest` command.

### 11.2.0

- Added `suggest` command.
- Added suggestion channel config to set where suggestions go.

### 11.1.1

- Updated `invite` command to use new short link.

### 11.1.0

- Added `starcount` command.
- Added tracking for user's star total in server.

### 11.0.0

- Refactor to no longer use `modulealias` package and enforce full imports.

## Version 10

### 10.4.3

- Fix error handling in `habitica` command.

### 10.4.2

- Dependency updates
- Removed `allcontributors` plugin.

### 10.4.1

- Restricted `leaderboard` command to display top 10.

### 10.4.0

- Added `leaderboard` command.

### 10.3.0

- Added `resetlevel` command.

### 10.2.7

- Fixed bug in rendering "last seen" on `level` embed.

### 10.2.6

- Fixed issue with events such as publishing announcements triggering the `MESSAGE_UPDATE` event.

### 10.2.5

- Updated broken links in various command to use new repository URL.

### 10.2.4

- Added new art to art list.

### 10.2.3

- Removed command usage tracking.

### 10.2.2

- Removed user count from `about` command.

### 10.2.1

- Removed `usage` command.

### 10.2.0

- Added database encryption plugin.

### 10.1.4

- Added new art to art list.

### 10.1.3

- Added new art to art list.

### 10.1.2

- Fixed art embed to render art name.

### 10.1.1

- Added new art to art list.
- Fixed wording error on `tickle` command.

### 10.1.0

- Added `emote` commands.

### 10.0.1

- Added instructions for how to use command to solve the `riddle`.

### 10.0.0

- Refactored commands to split into categories.

## Version 9

### 9.2.1

- Fixed message deletion and update embeds to substring the content if longer than Discord's maximum.

### 9.2.0

- Deprecated the harry potter themed commands.

### 9.1.2

- Removed the dynamic import of the `dotenv` package.

### 9.1.1

- Update contributor embed to use default colour.

### 9.1.0

- Fixed URL parsing in `caniuse` command.
- Deprecated the `profile` command.

### 9.0.2

- Added message link to `MESSAGE_UPDATE` embed.
- Converted `star` command to reply in channel instead of DM.

### 9.0.1

- Added new art to art list.

### 9.0.0

- Refactored commands to use enviroment variables for reaction emotes, instead of hardcoded values.

## Version 8 and Earlier

Due to improper versioning practises, change logs are not available for versions older than 9.0.0. Interested parties should review the GitHub commit history for changes prior to version 9.
