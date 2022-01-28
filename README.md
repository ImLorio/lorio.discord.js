<div align="center">
  <br />
  <p>
    <a href="https://discord.js.org"><img src="https://discord.js.org/static/logo.svg" width="546" alt="discord.js" /></a>
  </p>
  <br />
  <p>
    <a href="https://www.npmjs.com/package/lorio.discord.js"><img src="https://img.shields.io/npm/v/lorio.discord.js.svg?maxAge=3600&style=for-the-badge" alt="NPM version" /></a>
    <a href="https://www.npmjs.com/package/lorio.discord.js"><img src="https://img.shields.io/npm/dt/lorio.discord.js.svg?maxAge=3600&style=for-the-badge" alt="NPM downloads" /></a>
  </p>
  <p>
    <a href="https://nodei.co/npm/lorio.discord.js/"><img src="https://nodei.co/npm/lorio.discord.js.png?downloads=true&stars=true&compact=true" alt="NPM info" /></a>
  </p>
</div>

## INFORMATIONS
This package is a modified discord.js v11 package with some fix for user tokens

### To Do:
- ✔️ Fix channel error (`Cannot read properties of undefined (reading 'id')`)
- ✔️ Change User-Agent 
- ✔️ Add support for thread channel and Stage Voice channel (don't ignore it and declares as TextChannel or VoiceChannel).
- ❌ Add full support for thread channel and stage voice channel

## About
discord.js is a powerful [node.js](https://nodejs.org) module that allows you to interact with the
[Discord API](https://discord.com/developers/docs/intro) very easily.

- Object-oriented
- Predictable abstractions
- Performant
- 100% coverage of the Discord API

## Installation
**Node.js 6.0.0 or newer is required.**  
Ignore any warnings about unmet peer dependencies, as they're all optional.

Without voice support: `npm install lorio.discord.js`  
With voice support ([@discordjs/opus](https://www.npmjs.com/package/@discordjs/opus)): `npm install lorio.discord.js @discordjs/opus`  
With voice support ([opusscript](https://www.npmjs.com/package/opusscript)): `npm install lorio.discord.js opusscript`

### Audio engines
The preferred audio engine is @discordjs/opus, as it performs significantly better than opusscript. When both are available, discord.js will automatically choose @discordjs/opus.
Using opusscript is only recommended for development environments where @discordjs/opus is tough to get working.
For production bots, using @discordjs/opus should be considered a necessity, especially if they're going to be running on multiple servers.

### Optional packages
- [bufferutil](https://www.npmjs.com/package/bufferutil) to greatly speed up the WebSocket when *not* using uws (`npm install bufferutil`)
- [erlpack](https://github.com/hammerandchisel/erlpack) for significantly faster WebSocket data (de)serialisation (`npm install hammerandchisel/erlpack`)
- One of the following packages can be installed for faster voice packet encryption and decryption:
    - [sodium](https://www.npmjs.com/package/sodium) (`npm install sodium`)
    - [libsodium.js](https://www.npmjs.com/package/libsodium-wrappers) (`npm install libsodium-wrappers`)

## Example usage
```js
const Discord = require('lorio.discord.js');
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
* [Website](https://discord.js.org/) ([source](https://github.com/discordjs/website))
* [Documentation](https://discord.js.org/#/docs)
* [Guide](https://discordjs.guide/) ([source](https://github.com/discordjs/guide))
* [Discord.js Discord server](https://discord.gg/bRCvFy9)
* [Discord API Discord server](https://discord.gg/discord-api)
* [GitHub](https://github.com/ImLorio/lorio.discord.js)
* [NPM](https://www.npmjs.com/package/lorio.discord.js)
* [Related libraries](https://discordapi.com/unofficial/libs.html)

### Extensions
* [RPC](https://www.npmjs.com/package/discord-rpc) ([source](https://github.com/discordjs/RPC))

## Contributing
Before creating an issue, please ensure that it hasn't already been reported/suggested, and double-check the
[documentation](https://discord.js.org/#/docs).  
See [the contribution guide](https://github.com/discordjs/discord.js/blob/master/.github/CONTRIBUTING.md) if you'd like to submit a PR.

## Help
If you don't understand something in the documentation, you are experiencing problems, or you just need a gentle
nudge in the right direction, please don't hesitate to join our official [Discord.js Server](https://discord.gg/bRCvFy9).
