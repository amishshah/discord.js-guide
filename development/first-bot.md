# Your First Bot

Now it's time to develop your first bot! If you haven't already, please make sure you've
[created a bot account](../creating-a-bot-account.md) and have installed discord.js - the Getting
Started section should go through all of this.

We're also assuming that you've learned the basics of JavaScript, if you've not try taking a look
at the [CodeAcademy JavaScript course](https://www.codecademy.com/learn/javascript).

## A really basic bot

Assuming you're good to go, let's start coding! In the getting started chapter, we went through
creating a folder for your bot, creating a bot account (make sure you have its token) and installing
a proper editor.

Open the editor you've chosen and create a new file, naming it something like `bot.js`. Make sure you
save it in the folder you created for your bot.

One of the most basic bots you can create with discord.js is a simple ping-pong bot (you can copy this
code into your editor and save it.)

```js
const Discord = require('discord.js');
const client = new Discord.Client();

client.on('message', message => {
  if (message.content.startsWith('ping!')) {
    message.reply('pong!');
  }
});

client.on('ready', () => {
   console.log('I am ready!'); 
});

client.login('your bot token');
```

Replace `your bot token` with your bot's token, and open up a command prompt or terminal in your bot's folder.
Run `node bot.js` and try sending `ping!` to a text channel the bot is in.

### Breaking it down

Before we start to look at developing a more useful bot, let's have a look at what is happening:

```js
const Discord = require('discord.js');
const client = new Discord.Client();
```
This piece of code simply imports the discord.js library, and then creates a new Discord Client.

```js
client.on('message', message => {
  if (message.content === 'ping!') {
    message.reply('pong!');
  }
});
```
This piece of code adds a _"message"_ event listener. We'll talk more about message events later, but for now all you
need to know is that whenever the client receives a message, it also fires out a _message_ event. We can listen for this
event if we want our bot to react to messages.

This particular event listener receives a message object, and then it checks to see if the message that was sent was `ping!`.
If it was, then we reply to that message with `pong!`.

```js
client.on('ready', () => {
   console.log('I am ready!'); 
});
```
This is another event listener for the _ready_ event. Again, we'll talk about events later, but for now all you need to
know is that when the _ready_ event is fired, your bot is ready to start working.