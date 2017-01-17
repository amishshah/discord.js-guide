# Installing Discord.js (Linux)

Now that you've got your [bot account created](./creating-a-bot-account.html), we can start installing discord.js!

## TL;DR
* [Node.js v6 and above](https://nodejs.org/en/download/package-manager/)
* [Python 2.7](http://docs.python-guide.org/en/latest/starting/install/linux/)
* `npm install --save discord.js` in your bot's project folder
* Good to go!

## Pre-requisites
Make sure you have node.js v6 and above installed, [take a look here.](https://nodejs.org/en/download/package-manager/)

You'll also need Python 2.7, most linux distributions come with it anyway, but you can check if you have it by running
`python --version`. If this isn't 2.7, take a look at
[installing Python](http://docs.python-guide.org/en/latest/starting/install/linux/).

## Installing discord.js
Create a folder for your bot's code and then navigate to that folder in a terminal. We recommend that you also initialise
your bot project as an _npm module_, which you can do by running `npm init`, which starts a wizard that guides you through the
process. It makes distributing and managing your bot much easier in the future.

Install discord.js with `npm install --save discord.js`.

> If you want your bot to be able to play and receive audio in voice channels, also type
`npm install --global ffmpeg-binaries`.

You may see `UNMET PEER DEP` errors, ignore them. You can ensure discord.js is installed by running `npm list discord.js`.