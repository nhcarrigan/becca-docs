# Configure your Server

There are a number of options for configuring your server.

> [!NOTE]
> Config settings are set on a per-server basis. Only moderators with the "Manage Server" permission can change the settings.

## Global Configurations

The `/config set` slash command will allow you to configure Becca's general features and behaviour for your server.

| Setting              | Inputs                    | Description                                                                                                     |
| -------------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `appeal_link`        | `link: string`            | Provides `link` as the URL to appeal a ban, when sending a ban notification DM.                                 |
| `blocked`            | `user: User`              | Adds or removes `user` from the list of users not permitted to interact with Becca in your server.              |
| `emote_channels`     | `channel: Channel`        | Toggles whether `channel` should be set to emote-only (messages containing text or non-emotes will be deleted). |
| `hearts`             | `user: User`              | Toggles whether `user` should receive automatic heart reactions on their messages.                              |
| `report_channel`     | `channel: Channel`        | Will send message reports (through Becca's context command) to the `channel`.                                   |
| `sass_mode`          | `toggle: on \| off`       | Turns Becca's sass mode on or off.                                                                              |
| `suggestion_channel` | `channel: Channel`        | Suggestions made through `/community suggest` will be sent to the `channel`.                                    |
| `ticket_category`    | `category: GuildCategory` | The `category` under which new tickets should be opened. If not set, will deactivate the ticket system.         |
| `ticket_log_channel` | `channel: GuildText`      | The `channel` where closed tickets should be logged. If not set, will deactivate the ticket system.             |
| `ticket_role`        | `role: Role`              | The `role` to add to all new tickets, if desired. If not set, will default to anyone with admin permissions.    |

## Automod Settings

The `/automod set` command will allow you to configure Becca's automatic moderation.

The auto-moderation system will not run on any users who have the `Manage Messages` permission.

| Setting               | Inputs                                | Description                                                                                                         |
| --------------------- | ------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `allowed_links`       | `regex: Regex`                        | Adds or removes a regex to the list of allowed links. Links which match one of these will not count toward automod. |
| `antiphish`           | `action: none \| mute \| kick \| ban` | Sets the `action` to take when a user sends a scam link.                                                            |
| `automod_channels`    | `channel: Channel`                    | Adds or removes `channel` from the list of channels that are automodded.                                            |
| `automod_roles`       | `role: Role`                          | Adds or removes `role` from the list of roles that are ignored by automod.                                          |
| `link_message`        | `message: string`                     | Sets the message to be sent when a message containing a link is detected.                                           |
| `no_automod_channels` | `channel: Channel`                    | Adds or removes `channel` from the list of channels that are never automodded.                                      |
| `profanity_message`   | `message: string`                     | Sets the message to be sent when a message containing profanity is detected.                                        |

## Level Settings

The `/levels set` command allows you to adjust how Becca's levelling system works.

| Setting         | Inputs                      | Description                                                                      |
| --------------- | --------------------------- | -------------------------------------------------------------------------------- |
| `initial_xp`    | `points: number`            | New users joining your server will start with `points` experience, instead of 0. |
| `level_channel` | `channel: Channel`          | Sets where the level/role messages should be sent.                               |
| `level_ignore`  | `channel: Channel`          | Adds or removes `channel` from the list of channels not to track experience in.  |
| `level_message` | `message: string`           | Sets the custom `message` to be sent when a user earns a level.                  |
| `level_roles`   | `role: Role, level: number` | Sets `role` to be assigned when a user reaches `level`.                          |
| `level_style`   | `toggle: text \| embed`     | Toggles the level/role messages between text and embed.                          |
| `levels`        | `toggle: on \| off`         | Toggles the level system on and off.                                             |
| `role_message`  | `message: string`           | Sets the custom `message` to be sent when a user earns a level role.             |

## Log Settings

The `/log set` command allows you to set which channel Becca should use for logging specific Discord events.

| Setting             | Inputs             | Description                                                        |
| ------------------- | ------------------ | ------------------------------------------------------------------ |
| `member_events`     | `channel: Channel` | Sets where member update events (e.g. nickname changes) should go. |
| `message_events`    | `channel: Channel` | Sets where message events (e.g. edits/deletes) should go.          |
| `moderation_events` | `channel: Channel` | Sets where moderation events (e.g. kicks/bans) should go.          |
| `thread_events`     | `channel: Channel` | Sets where thread events (e.g. create/archive) should go.          |
| `voice_events`      | `channel: Channel` | Sets where voice events (e.g. join/leave) should go.               |

## Welcome Settings

The `/welcome set` command allows you to configure how Becca says hello and goodbye to your server members.

| Setting           | Inputs                  | Description                                               |
| ----------------- | ----------------------- | --------------------------------------------------------- |
| `custom_welcome`  | `message: string`       | The `message` to be sent when someone joins your server.  |
| `depart_channel`  | `channel: Channel`      | The `channel` to send goodbye messages in.                |
| `join_role`       | `role: Role`            | The `role` to assign when someone joins your server.      |
| `leave_message`   | `message: string`       | The `message` to be sent when someone leaves your server. |
| `welcome_channel` | `channel: Channel`      | The `channel` to send welcome messages in.                |
| `welcome_style`   | `toggle: text \| embed` | Sets whether join/leave messages should be text or embed. |

## Resetting a Setting

Each configuration group will have a `reset` command which allows you to reset that setting to the default value.

## Viewing Your Config

The `view` command under each configuration group will display the values for the given setting

## Placeholders

Certain settings that allow for custom text also allow for placeholders to use dynamic values from the event.

| Setting          | Placeholder     | Value                                  |
| ---------------- | --------------- | -------------------------------------- |
| `role_message`   | `{user}`        | The user's username and discriminator. |
|                  | `{role}`        | The name of the role earned.           |
|                  | `{@user}`       | Mentions the user (does not ping).     |
|                  | `{@role}`       | Mentions the role (does not ping).     |
| `level_message`  | `{user}`        | The user's username and discriminator. |
|                  | `{level}`       | The level reached.                     |
|                  | `{@user}`       | Mentions the user (does not ping).     |
| `custom_welcome` | `{@username}`   | The user's username.                   |
|                  | `{@servername}` | The server's name.                     |
| `leave_message`  | `{@username}`   | Mentions the user (does not ping).     |
|                  | `{@servername}` | The server's name.                     |
