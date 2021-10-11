# Configure your Server

The `/config set` slash command will allow you to configure Becca's features and behaviour for your server.

| Setting                | Value                          | Description                                                                                                                                                                                                |
| ---------------------- | ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Allowed Link Channels  | `channel: Channel`             | This will add or remove the `channel` to the list of channels to _not_ auto-delete links in.                                                                                                               |
| Allowed Link Regex     | `regex: string`                | This will add a regex that prevents links from being deleted if they match.                                                                                                                                |
| Allowed Link Roles     | `role: Role`                   | This will prevent deleting links for members who have the `role`.                                                                                                                                          |
| Anti-link Channels     | `channel: Channel`             | This will tell Becca to automatically delete messages containing links for that channel. Use `all` to turn this on for every channel.                                                                      |
| Blocked Users          | `user: User`                   | This will prevent the `user` from using any of Becca's commands.                                                                                                                                           |
| Custom Leave Message   | `message: string`              | This will set the message to be sent when a user leaves your server. In the message, `{@username}` will be replaced with the user's mention, and `{@servername}` will be replaced with your server's name. |
| Custom Welcome Message | `message: string`              | This will set the message to be sent when a user joins your server. In the message, `{@username}` will be replaced with the user's mention, and `{@servername}` will be replaced with your server's name.  |
| Heart Users            | `user: User`                   | This will add or remove the `user` to the list of people who receive heart reactions on their messages.                                                                                                    |
| Join/Leave Channel     | `channel: Channel`             | This will tell Becca where to send messages when users join or leave your server.                                                                                                                          |
| Level Log Channel      | `channel: Channel`             | This will tell Becca where to send messages when a user levels up or earns a level role.                                                                                                                   |
| Level System           | `on \| off`                    | This will enable or disable the level system.                                                                                                                                                              |
| Level-Assigned Roles   | `level: number`, `role: @role` | This will tell Becca to give users the `role` when they reach the `level`.                                                                                                                                 |
| Level Ignore Channels  | `channel: Channel`             | This will tell Becca not to grant experience for messages sent in the provided channel. Use the command with the channel again to re-enable experience.                                                    |
| Link Delete Message    | `message: string`              | This tells Becca what message to send when she deletes a link.                                                                                                                                             |
| Moderation Log Channel | `channel: Channel`             | This tells Becca where to send logs of moderation activities.                                                                                                                                              |
| Muted Role             | `role: Role`                   | When using the `mute` and `unmute` commands, this is the `role` that will be added or removed. To make this effective, you should ensure `role` does not have permissions to send messages in channels.    |
| Report Channel         | `channel: Channel`             | This tells Becca where to send the messages reported with the `report` context menu. If this is not set, Becca will refuse to perform the command.                                                         |
| Role on Join           | `role: Role`                   | Becca will assign this `role` when a member joins your server. If you have membership screening enabled, she will not assign the `role` until they complete it.                                            |
| Sass Mode              | `on \| off`                    | This enables specific sassy responses from Becca when the content of a message matches specific conditions.                                                                                                |
| Self-Assignable Roles  | `role: Role`                   | Adds or removes the `role` to the list that members can assign themselves.                                                                                                                                 |
| Suggestion Channel     | `channel: Channel`             | Sets the channel where suggestions made with the `suggest` command are sent.                                                                                                                               |
| Thanks System          | `on \| off`                    | Enables or disables the feature where Becca recognises people who are thanked.                                                                                                                             |

> [!NOTE]
> Config settings are set on a per-server basis. Only moderators with the "Manage Server" permission can change the settings.

## Resetting a Setting

The `/config reset` command will take any of the above options and reset it to the default value.

## Viewing Your Config

The `/config view` command will display the values for the given setting. Choosing `Global Settings` will show all of your values, with the following settings being represented by the number of entries for that setting. These settings can be selected individually to see those entries:

`Allowed Link Channels`, `Allowed Link Regex`, `Anti-link Channels`, `Blocked Users`, `Heart Users`, `Level-assigned Roles`, `Self-assigned Roles`.
