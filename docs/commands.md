# Commands

### uptime
Shows the time where the bot is running for.
#### aliases
 - up
#### permissions
 - user

---
### stop
Stops the bot and trys to restart.
#### aliases
 - exit
 - shutdown
 - restart
#### permissions
 - owner

 ---
### ping
Display the latency between server and bot.
#### aliases
 - p
 - pong
#### permissions
 - user

 ---
### help
Send an information message with commands ith descriiption.
#### aliases
 - h
#### permissions
 - user

 ---
### info
Send an information message content about the bot and the guild.
#### aliases
 - i
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