# hubot-help

A hubot script to show available hubot commands per module.

See [`src/help.coffee`](src/help.coffee) for full commands reference.

## Details

The current implementation of hubot-help lists all commands in all scripts and modules, resulting in a massive list of commands pushing all other messages off the screen.

Instead, the basic plan is to first return a list of modules by default, and to provide commands only when specified.

This MUST work with the current standard without requiring changes to the scripts themselves.

## Planned Improvements

- [ ] Support for module descriptions, will be listed alongside module names and with commands for a single module
- [ ] Support for "friendly" module names, will default to file name if not present
- [ ] Querying the complete commands list directly (ie. searching commands across all modules/scripts)
- [ ] Querying/Filtering at any level
- [ ] Configurable output - modules/scripts on one line or one per line

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
