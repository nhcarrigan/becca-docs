# Owner Commands

> [!WARNING]
> The following commands are restricted to Becca's owner, by Discord ID. These commands will not work for users (not even server admins). They are only documented here for transparency, and for contributors who are working on the code locally.

Becca has specific owner-only commands, which are message based to avoid cluttering the slash command UI with things that users cannot run.

- `Naomi fish <link>`: Used to report a phishing `link` to the database that we are using.

- `Naomi purge <data> <id>`: Cleans all of the user's data (based on `id`) for the given `data` type. This is used to comply with data deletion and opt-out requests.

- `Naomi register`: Sends the current slash command JSON to Discord, updating the registered commands.

- `Naomi unregister <command>`: Unregisters a given command from Discord.

- `Naomi view`: Provides a list of all registered commands (used to confirm the `register` and `unregister` commands).
