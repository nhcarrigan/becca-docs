# File Structure

Becca's code is intentionally kept modular to reduce file size and cognitive complexity of the code. However, this can mean that the file tree itself is a bit confusing, at times.

This document will break down the file structure and should be used when creating new files.

All code goes in the `src` directory.

## `commands` Directory

This directory holds all of the slash command code. These commands are each an exported object which *shares the name of the file* - this is essential for the dynamic import process.

For example, the file `becca.ts` must have `export const becca` as the command.

Command objects have two properties:

- `data`: This is the slash command data object, created with the `discordjs/builder` tool.
- `run`: This is the logic for the command. The *only* logic that goes in here is the sub-command `switch` logic. Everything else should go in a subcommand module.

## `config` Directory

These are the various config files for the bot. These control the global settings.

## `contexts` Directory

This directory holds all of the context command (right click menu) code. Like the `commands`, the file name must match the export name.

Contexts take the same structure, with a `data` property representing the component object and `run` holding the logic. These, however, do not need modules for the logic and all of the runtime execution is held in the `run` property directly.

## `database` Directory

This holds all of the database schema and logic, with `connectDatabase.ts` instantiating the MongoDB collection.

## `events` Directory

This directory holds all of the modules for the Discord Gateway event listeners.

## `interfaces` Directory

This is where all of the custom type definitions go.

## `listeners` Directory

This is where Becca's custom listeners go. Like commands, listeners need the export to match the file name.

A listener has three properties:

- `name`: The name of the listener.
- `description`: A brief description of what the listener does.
- `run`: The logic for the listener.

## `modules` Directory

This is where the bulk of the logic will exist. Modules are code that runs specifically in one area, such as a command.

Slash command logic all goes in `modules/command/subcommands`.

File names and export names should be descriptive, and while ideally they will match it is not a requirement.

## `server` Directory

The `server` directory contains all of the logic for the basic HTTP server. The server is used for uptime monitoring, and for the dashboard to fetch data.

## `utils` Directory

The `utils` directory is similar to the `modules` directory, but is used for logic bits that have a more global scope, such as the error handling wrapper.
