# Rehkbot

Valorant Discord bot

<p><a href="https://heroku.com/deploy" rel="nofollow"><img src="https://camo.githubusercontent.com/c0824806f5221ebb7d25e559568582dd39dd1170/68747470733a2f2f7777772e6865726f6b7563646e2e636f6d2f6465706c6f792f627574746f6e2e706e67" alt="Deploy to Heroku" data-canonical-src="https://www.herokucdn.com/deploy/button.png" style="max-width:100%;"></a></p>

## Requirements

- Python 3.6 and up - https://www.python.org/downloads/
- git - https://git-scm.com/download/

## How to setup discord bot

Make a bot [here](https://discordapp.com/developers/applications/me) and grab the token
![Image_Example1](https://i.imgur.com/iV2WWQz.png)

### How to install modules

```
for windows:
python -m pip install -r requirements.txt

for linux:
python3 -m pip install -r requirements.txt
```

### How to setup Webhooks

click [here](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks) to learn how to setup webhooks

### ENV

rename `.env.example` to `.env` then store your token and some other private info like this:

```
DISCORD_TOKEN=
vlr_news_webhook_url =
vlr_matches_webhook_url =

```

## FAQ

Q: I don't see my bot on my server!<br>
A: Invite it by using this URL: https://discordapp.com/oauth2/authorize?client_id=CLIENT_ID&scope=bot<br>
Remember to replace **CLIENT_ID** with your bot client ID

### PM2

PM2 is an alternative script provided by NodeJS, which will reboot your bot whenever it crashes and keep it up with a nice status. You can install it by doing `npm install -g pm2` and you should be done. Keep in mind that this PM2 file is made to work on my own Linux instance, you might need to change the `interpreter` value.

```
# Start the bot
pm2 start pm2.json

# Tips on common commands
pm2 <command> [name]
  start <name of bot>   Run the bot again if it's offline
  list                    Get a full list of all available services
  stop <name of bot>     Stop the bot
  reboot <name of bot>   Reboot the bot
```

### Docker

Docker is an alternative to run the bot 24/7 and always reboot again whenever it crashed. You can find the install manual [here](https://docs.docker.com/install/). You don't _have_ to get it, but if you're used to having Docker, it's available at least.

```
# Build and run the Dockerfile
docker-compose up -d --build

# Tips on common commands
docker-compose <command>
  ps      Check if bot is online or not (list)
  down    Shut down the bot
  reboot  Reboot the bot without shutting it down or rebuilding
  logs    Check the logs made by the bot.
```
