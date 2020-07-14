## About
sts-discordjs is a powerful [node.js](https://nodejs.org) module that allows you to interact with the
[Discord API](https://discordapp.com/developers/docs/intro) very easily.

- Object-oriented
- Predictable abstractions
- Performant
- 100% coverage of the Discord API

## Installation
**Node.js 6.0.0 or newer is required.**  
Ignore any warnings about unmet peer dependencies, as they're all optional.

Without voice support: `npm install sts-discordjs`  

### Optional packages
- [bufferutil](https://www.npmjs.com/package/bufferutil) to greatly speed up the WebSocket when *not* using uws (`npm install bufferutil`)
- [erlpack](https://github.com/hammerandchisel/erlpack) for significantly faster WebSocket data (de)serialisation (`npm install hammerandchisel/erlpack`)
- One of the following packages can be installed for faster voice packet encryption and decryption:
    - [sodium](https://www.npmjs.com/package/sodium) (`npm install sodium`)
    - [libsodium.js](https://www.npmjs.com/package/libsodium-wrappers) (`npm install libsodium-wrappers`)

## Example usage
```js
const Discord = require('sts-discordjs');
const client = new Discord.Client();

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on('message', msg => {
  if (msg.content === 'ping') {
    msg.reply('pong');
  }
});

client.login('token');
```

## Links
* [Sigma.js Discord server](https://discord.gg/yJp2wTH)
* [Discord API Discord server](https://discord.gg/discord-api)
* [GitHub](https://github.com/hamster-0001/sigma.js)
* [Related libraries](https://discordapi.com/unofficial/libs.html)

## Help
If you don't understand something in the documentation, you are experiencing problems, or you just need a gentle
nudge in the right direction, please don't hesitate to join our official [Sigma.js Server](https://discord.gg/yJp2wTH).

## Credits and Disclaimers
This library is a rework of the original Discord.js v11. It has been rewritten to support the change from discordapp.com to discord.com. 
