<div align="center">

  <p>
    <a href="https://www.npmjs.com/package/discord-confirm"><img src="https://img.shields.io/npm/v/discord-confirm?maxAge=3600" alt="NPM version" /></a>
<a href="https://www.npmjs.com/package/discord-confirm"><img src="https://img.shields.io/npm/dt/discord-confirm?maxAge=3600" alt="NPM downloads" /></a>
  </p>

  <p>
    <a href="https://www.npmjs.com/package/discord-confirm"><img src="https://nodei.co/npm/discord-confirm.png?downloads=true&stars=true" alt="NPM Banner"></a>
  </p>
</div>

## Installation
```sh
$ npm install discord-confirm
```

<h1>DISCORD.JS</h2>

## Example

## Confirm
```js
//INITIALIZATION
const { confirm } = require("discord-confirmation")
//EXAMPLE OF SENDING MESSAGE
message.channel.send("Do you want to send the message?").then(async (message) => {
    const reactions = await confirm(message, message.author, ["✅", "❌"], 10000); //TIME IS IN MILLISECONDS
    if(reactions === "✅") {
        message.channel.send("Hello, my friend")
    }
    if(reactions === "❌") {
        return;
    }
    else {
        console.log("Timed Out")
    }
})
```