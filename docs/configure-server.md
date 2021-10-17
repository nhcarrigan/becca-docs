# Configure your Server

There are a number of options for configuring your server.

> [!NOTE]
> Config settings are set on a per-server basis. Only moderators with the "Manage Server" permission can change the settings.

## Global Configurations

The `/config set` slash command will allow you to configure Becca's features and behaviour for your server.

| Setting                | Value                          | Description                                                                                                                                                                                                |
| ---------------------- | ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Blocked Users          | `user: User`                   | This will prevent the `user` from using any of Becca's commands.                                                                                                                                           |
| Custom Leave Message   | `message: string`              | This will set the message to be sent when a user leaves your server. In the message, `{@username}` will be replaced with the user's mention, and `{@servername}` will be replaced with your server's name. |
| Custom Welcome Message | `message: string`              | This will set the message to be sent when a user joins your server. In the message, `{@username}` will be replaced with the user's mention, and `{@servername}` will be replaced with your server's name.  |
| Heart Users            | `user: User`                   | This will add or remove the `user` to the list of people who receive heart reactions on their messages.                                                                                                    |
| Join/Leave Channel     | `channel: Channel`             | This will tell Becca where to send messages when users join or leave your server.                                                                                                                          |
| Level Log Channel      | `channel: Channel`             | This will tell Becca where to send messages when a user levels up or earns a level role.                                                                                                                   |
| Level System           | `on \| off`                    | This will enable or disable the level system.                                                                                                                                                              |
| Level-Assigned Roles   | `level: number`, `role: @role` | This will tell Becca to give users the `role` when they reach the `level`.                                                                                                                                 |
| Level Ignore Channels  | `channel: Channel`             | This will tell Becca not to grant experience for messages sent in the provided channel. Use the command with the channel again to re-enable experience.                                                    |
| Muted Role             | `role: Role`                   | When using the `mute` and `unmute` commands, this is the `role` that will be added or removed. To make this effective, you should ensure `role` does not have permissions to send messages in channels.    |
| Report Channel         | `channel: Channel`             | This tells Becca where to send the messages reported with the `report` context menu. If this is not set, Becca will refuse to perform the command.                                                         |
| Role on Join           | `role: Role`                   | Becca will assign this `role` when a member joins your server. If you have membership screening enabled, she will not assign the `role` until they complete it.                                            |
| Sass Mode              | `on \| off`                    | This enables specific sassy responses from Becca when the content of a message matches specific conditions.                                                                                                |
| Self-Assignable Roles  | `role: Role`                   | Adds or removes the `role` to the list that members can assign themselves.                                                                                                                                 |
| Suggestion Channel     | `channel: Channel`             | Sets the channel where suggestions made with the `suggest` command are sent.                                                                                                                               |

## Automod Settings

The `/automod set` command will allow you to configure Becca's automatic moderation.

The auto-moderation system will not run on any users who have the `Manage Messages` permission.

| Setting                  | Value              | Description                                                                                                                                                                                     |
| ------------------------ | ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Automodded Channels      | `channel: Channel` | Adds or removes a channel to the list of channels that Becca will automatically moderate. Pass `all` to set this to all channels.                                                               |
| Automod Ignored Channels | `channel: Channel` | Adds or removes a channel to the list of channels that Becca will not automatically moderate. Pass `all` to set this to all channels. This setting overrides the `Automodded Channels` setting. |
| Automod Exempt Roles     | `role: Role`       | Adds or removes a role to the list of roles that are exempt from auto-moderation.                                                                                                               |
| Allowed Link Regex       | `regex: string`    | Adds or removes a regex that will be used to match approved links.                                                                                                                              |
| Link Delete Message      | `message: string`  | Sets the message that will be sent to users who have links removed.                                                                                                                             |
| Profanity Delete Message | `message: string`  | Sets the message that will be sent to users who have profanity removed.                                                                                                                         |

The `/automod toggle` command will toggle specific auto-moderation listeners on and off.

| Setting             | Description                                            |
| ------------------- | ------------------------------------------------------ |
| Link Detection      | Becca will remove any message that contains a link.    |
| Profanity Detection | Becca will remove any message that contains profanity. |

## Log Settings

The `/log set` command allows you to set which channel Becca should use for logging specific Discord events.

| Setting           | Description                                                                |
| ----------------- | -------------------------------------------------------------------------- |
| Message Events    | Logs related to message edits and deletions.                               |
| Voice Events      | Logs related to joining, leaving, muting, and deafening in a voice channel |
| Thread Events     | Logs related to creating, archiving, and deleting threads.                 |
| Moderation Events | Logs related to kicking, warning, banning, or muting a user.               |
| Member Events     | Logs related to membership screening and member record updates.            |

## Resetting a Setting

All three configuration groups have a `reset` command to reset the value of a setting to the default (usually turning off the feature).

## Viewing Your Config

The `view` command under each configuration group will display the values for the given setting. Choosing `Global Settings` will show all of your values, while specific values are available to view nested settings.
