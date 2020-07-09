# Commands

### uptime
Shows since how long the bot has been running for.
#### aliases
 - up
#### permissions
 - user

---
### stop
Stops the bot and tries to restart.
#### aliases
 - exit
 - shutdown
 - restart
#### permissions
 - owner

 ---
### ping
Displays the latency between the server and bot.
#### aliases
 - p
 - pong
#### permissions
 - user

 ---
### help
Sends an information message with the list of commands and their aliases.
#### aliases
 - h
#### permissions
 - user

 ---
### info
Sends an information message about the bot and its data.
#### aliases
 - i
#### permissions
 - user

 ---
### code
Sends a message with a template to send code snippets. 
#### aliases
\<none>
#### permissions
 - user

---
### ask
Sends a message with the 'Don't ask to ask' response.
#### aliases
\<none>
#### permissions
 - user

 ---
### math
Sends a message with the result of a calculation.
#### aliases
 - m
 - calc
#### permissions
 - user

---
### phpdoc
Sends a message with the result of a search querry.
#### aliases
 - php
#### permissions
 - user

## Create Commands

The [commands folder](https://github.com/PopperDevs/PopperBot/tree/master/commands) contains every command for the bot. Each command has its own folder, and an index.js in it. If a command contains a subcommand, a file with the subcommand name is created inside the folder.

### Template for a command

```javascript
const { permissionType, commandType } = require('../../lib/permissions');

module.exports = {
  name: 'example',
  aliases: ['alias1', 'alias2'],
  type: commandType.base.name,
  permissions: permissionType.user,
  template: 'example',
  handler({ Discord, client, message, args }) {
    message.channel.send('This is an example command.');
  },
};
```