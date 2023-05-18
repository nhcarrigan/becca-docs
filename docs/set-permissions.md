# Set Becca's Permissions

Discord's permission system is very powerful, but can also be very confusing.

By default, when you invite Becca to your server she will ask for the following permissions:

- Manage Server

- Manage Roles

- Manage Channels

- Kick Members

- Ban Members

- View Channels

- Read Messages

- Send Messages

- Manage Messages

- Embed Links

- Attach Files

- Read Message History

- Add Reactions

- Use External Emojis

- Manage Nicknames

- Moderate Members

- View Audit Log

- Manage Webhooks

All of these permissions are necessary for her features to work. Disabling any of these will cause unexpected errors to occur.

> [!NOTE]
> The permissions for interaction responses (slash commands) is a bit tricky, and in some cases the permissions applied to your @everyone role take effect. A known instance of this is that if @everyone is denied the `Use External Emojis` permission, then Becca's attempts to use external emojis will fail regardless of her permissions level.

## Integration Role

When you add a bot to your server that requires specific permissions, Discord will create a special role for that bot. The role will have the same name as the bot.

In this case, the role would be named `Becca Lyria`. Any changes to the permissions for the bot should be made by editing the role's settings.

## Role Hierarchy

One of Becca's features is a configurable list of roles your server members can assign/unassign for themselves. In order for Becca to be able to manage these roles, the integration role must be _higher_ than **all** of the self-assignable roles in your server permissions list.

Becca must also be higher than any roles you want to assign to members that she should be able to moderate (kick, ban, etc).

## Channel Overrides

There is a good chance you have specific channel permissions in your server. An example of this would be a `staff-chat` channel that only moderators can see.

If you disable any permissions on a channel for the `@everyone` role, they _must_ be explicitly granted on that channel to Becca's integration role. Failing to do this can lead to unexpected behaviour.

## Validating Permissions

If Becca is not responding in the way you expect, you can run the `/misc permissions` command to confirm that you have granted all of the permissions she needs to function.

## Administrator Permissions

> [!WARNING]
> Granting the administrator permission to a bot is a dangerous thing to do and can open your server up to threats such as nuking, raids, or mass bans.

If you are not comfortable with managing permissions, or are confused with the channel overrides, granting the administrator permission to Becca's integration role should prevent any issues.

It is important to understand that there are risks with granting a bot the administrator permission. While we strive to provide the best bot experience for you, in the event of a compromising attack on our infrastructure your server could potentially be vulnerable if you grant the administrator permission. Do so with care.

We recommend joining our [support server](https://chat.naomi.lgbt) so we can assist with permission questions, rather than enabling admin.
