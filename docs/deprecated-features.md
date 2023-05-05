# Deprecated Features

This page documents former features which have been deprecated, including the version that deprecated the feature and the reason for removal.

- `purge` _(deprecated in 6.9.1)_ - Removed due to Discord API limitations on the age at which messages could no longer be bulk deleted.

- `inulove` _(deprecated in 6.10.2)_ - Removed as incomplete, not used enough to warrant completion.

- `inuquote` _(deprecated in 6.10.2)_ - Removed as incomplete, not used enough to warrant completion

- `optout` _(deprecated in 7.0.8)_ - Removed as unused, unneeded for GDPR compliance.

- `block` _(deprecated in 7.1.0)_ - Removed as blocking users became server-specific

- `profile` _(deprecated in 9.0.3)_ - Type definition conflicts with mongoose, and lack of usage.

- `hpchar` _(deprecated in 9.2.0)_ - API no longer available.

- `hpsort` _(deprecated in 9.2.0)_ - API no longer available.

- `hpspell` _(deprecated in 9.2.0)_ - API no longer available.

- `usage` _(deprecated in 10.2.1)_ - Unused, and caused extraneous database calls.

- `contributors` _(deprecated in 10.2.5)_ - Removal of all-contributors integration, issues with http request.

- `adventure` _(deprecated in 11.4.0)_ - Removed due to noops API outages and unreliability.

- `challenge` _(deprecated in 11.4.0)_ - Removed due to noops API outages and unreliability.

- `maze` _(deprecated in 11.4.0)_ - Removed due to noops API outages and unreliability.

- `riddle` _(deprecated in 11.4.0)_ - Removed due to noops API outages and unreliability.

- `title` _(deprecated in 11.4.0)_ - Removed due to noops API outages and unreliability.

- `Emote Commands` _(boop, hug, tickle) (deprecated in 13.0.0)_ - Removed during a refactor of Becca's personality.

- `listeners` command _(deprecated in 14.0.0)_ - Removed as extraneous, listeners are documented here.

- `support` command _(deprecated in 14.0.0)_ - Rolled in to the `help` command.

- `levelscale` command _(deprecated in 14.0.0)_ - Available in the docs, removed to prevent noise in the channel where the command is called.

- `close` command _(deprecated in 14.0.0)_ - Removed as unneeded with refactor of `mute/unmute` logic.

- `moderator_role` config setting _(deprecated in 14.0.0)_ - Removed as unneeded with refactor of `mute/unmute` logic.

- `compliment` command _(deprecated in 14.0.0)_ - Data was not always logical.

- `echo` command _(deprecated in 14.0.0)_ - Was restricted to bot owner and unused.

- `jobs` command _(deprecated in 14.0.0)_ - Poorly written, not worth the overhead for refactoring.

- `maths` command _(deprecated in 14.0.0)_ - Unused, allowed for removal of dependency.

- `search` command _(deprecated in 14.0.0)_ - Poorly written, not worth the overhead for refactoring.

- `dnd` commands _(deprecated in 14.0.0)_ - Poorly written, not worth the overhead for refactoring.

- `pokemon` command _(deprecated in 14.0.0)_ - Poorly written, not worth the overhead for refactoring.

- `fortune` command _(deprecated in 14.0.0)_ - Removed due to lack of data needed for functionality.

- `kirby` command _(deprecated in 14.0.0)_ - Lack of use.

- `piglatin` command _(deprecated in 14.0.0)_ - Extraneous, lack of use.

- `roll` command _(deprecated in 14.0.0)_ - Extraneous, lack of use.

- ~~`orbit` command _(deprecated in 16.0.0)_ - Privacy concerns.~~ Restored in 17.2.0

- `guess` command _(deprecated in 16.0.0)_ - Did not migrate well to slash commands.

- `nhcarrigan list` command _(deprecated in 17.8.0)_ - No longer needed with verification in place.

- `nhcarrigan serverinfo` command _(deprecated in 17.8.0)_ - No longer needed with verification in place.

- `nhcarrigan leave` command _(deprecated in 17.8.0)_ - No longer needed with verification in place.

- `/community role` command _(deprecated in 18.6.0)_ - Removed in favour of the `/reactionrole` system.

- `/games habitica` command _(deprecated in 22.0.0)_ - Removed due to lack of use.

- `/misc orbit` command _(deprecated in 22.0.0)_ - Removed due to discontinuation of platform use.

## Temporary Deprecations

These features have been temporarily removed, but are planned for a future version.

- `github` command _(deprecated in 14.0.0)_ - May restore in a future version after implementing proper ratelimiting.

- `wiki` command _(deprecated in 14.0.0)_ - May restore in a future version using the Wikipedia API.

- ~~`habitica` command _(deprecated in 14.0.0)_ - Removed due to cognitive complexity, may restore with a new approach.~~ Restored in 17.2.0

- `reactionrole add` command _(deprecated in 20.0.0)_ - Removed due to type definition errors.

- `reactionrole remove` command _(deprecated in 20.0.0)_ - Removed due to type definition errors.

- server-specific command tracking _(deprecated in 20.1.0)_ - Removed for stricter privacy, and lack of continued need for data.
