# Tyrn Bot

My first Discord bot, and the first project I ever built. It is archived and no longer maintained, but I'm keeping it as a reminder of where I started.

Built with [discord.js](https://discord.js.org) v13, MongoDB (mongoose) and Express.

## Features

- **Moderation:** ban, kick, timeout, untimeout, clear, lock, unlock, nuke, tickets
- **Giveaways:** start, list and manage giveaways (persisted in MongoDB)
- **Server config:** auto-role, button roles, member join/leave logs, ignored channels, custom tags, per-user language
- **Info:** avatar, user, server and bot info
- **Fun and misc:** memes, russian roulette, add-emoji, NSFW, ping, invite
- **Owner tools:** eval and remote control
- **Extras:** Top.gg stats and vote webhook, English and Turkish translations

Every command works both as a slash command and as a prefix command (mention the bot, e.g. `@Tyrn ping`).

## Project structure

```
base/        Client (Tyrn.js) and the Command base class
commands/    One file per command, grouped by category
events/      Discord event handlers, loaded automatically
helpers/     Giveaways, logger, Top.gg
mongoose/    Database connection and models
translates/  en / tr language files
util/        Slash command loader
```

## Running it

Requires Node.js 16.9+ and a MongoDB database.

```bash
npm install
```

Create a `.env` file:

```
token=
mongoose=
errorHook=
cmdLogHook=
topggAuth=
topggToken=
```

Then edit `config.json` (client ID, owner IDs, support server) and run:

```bash
npm start
```

## Notes

This was written before I used linters, formatters or tests, and it shows in a few places. I left it as it was on purpose.
