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