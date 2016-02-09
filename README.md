# hubot-help

A hubot script to show available hubot commands per module.

See [`src/help.coffee`](src/help.coffee) for full commands reference.

## Details

The current implementation of hubot-help lists all commands in all scripts and modules, resulting in a massive list of commands pushing all other messages off the screen.

Instead, the basic plan is to first return a list of modules by default, and to provide commands only when specified.

This MUST work with the current standard without requiring changes to the scripts themselves.

## Planned Improvements

- [ ] Module descriptions
- [ ] Friendly module names
- [ ] Search modules
- [ ] Search commands of single module
- [ ] Search all commands

### Module Descriptions

The current standard includes a "Description" section in the script header, usually short.
Include these descriptions (perhaps truncated) alongside names when listing modules, and as part of the output when listing commands.

### Friendly Module Names

Support a "Friendly Name" or "Module Name" section in the script header that contains a more user-friendly module name.
Return the friendly name if present, else list the script's file name as usual.

### Search Modules

Make it possible to filter/search the list of modules when an incomplete name is provided.

### Search commands of a single module

As "Search Modules" but for commands of a module.

### Search All Commands

Implement a `hubot help search` command that searched the entire list of commands.
Something like `hubot help search *` should return the entire list as per the original `hubot help`.

## Installation

In hubot project repo, run:

`npm install hubot-help --save`

Then add **hubot-help** to your `external-scripts.json`:

```json
["hubot-help"]
```

## Sample Interaction

```
user1>> hubot help
hubot>> hubot help - Displays all of the help commands that Hubot knows about.
hubot>> hubot help <query> - Displays all help commands that match <query>.

```
