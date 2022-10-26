# Telegram Psychological Bot
A [Telegram](https://telegram.org) bot based on [aiogram](https://github.com/aiogram/aiogram) and [aiohttp](https://github.com/aio-libs/aiohttp) with cloud-based NoSQL-database [MongoDB](https://github.com/mongodb/mongo) implemented through [pymongo](https://github.com/mongodb/mongo-python-driver) package. 

The main mission of the bot - helping people (especially developers) to prevent burnout and depression. The bot allows:
- passing the psychological tests (only **The Beck Depression Inventory Test** `BDI-II` currently) with a user-friendly interface based on the Telegram inline keyboard.
- viewing dynamics changes (by plots implemented by [matplotlib](https://github.com/matplotlib/matplotlib) and [seaborn](https://github.com/mwaskom/seaborn)) of a user's mental condition (time-series of tests results) to control it and notice patterns.
- getting human-readable interpretations of tests result for a better understanding own mental condition.

## Requirements
1. Python3.9 or newer.
2. [Pyenv](https://github.com/pyenv/pyenv)
3. [MongoDB Atlas](https://github.com/mongodb/mongodb-atlas-cli)

## Installation
I created a Bash script that provides a simple and quick initialization of the bot. The script creates and activates a virtual environment, installs packages from `requirements.txt`, replaces constants with private access tokens for **Telegram Bot API** and **MongoDB**, and starts the bot. 

**The only thing you need is to run an `init.sh` file by the following command in your CLI:**
```
$ git clone https://github.com/annagerd/psybot.git
$ cd psybot
$ ./init.sh YOUR_TELEGRAM_BOT_TOKEN YOUR_MONGO_DB_CONNECTION_STRING
```
1. `YOUR_TELEGRAM_BOT_TOKEN` is a **Telegram Bot Access Token**. There is a getting token [here](https://t.me/BotFather) through creating a new Telegram bot.
2. `YOUR_MONGO_DB_CONNECTION_STRING` is a connection string for **MongoDB** that is accessible after the MongoDB Cluster creation. [See details](https://www.mongodb.com/docs/guides/atlas/connection-string).

## References
- [Aiogram 3 docs](https://docs.aiogram.dev/en/dev-3.x/index.html). This version is used in my project.
- [Aiogram 2 docs](https://docs.aiogram.dev/en/latest/index.html). I don't use this version here, but the docs of the second version are also useful because of a lot of useful information and advices that is still actual for also the third version.
- [MongoDB docs](https://www.mongodb.com/docs/develop-applications). Full MongoDB docs.
- [MongoDB Python Start Guide](https://www.mongodb.com/languages/python). Simple instructions about using MongoDB with Python programming language.
- [MongoDB References](https://www.mongodb.com/docs/manual/reference). References that can help you to work with Mongo API.
- [Matplotlib References](https://matplotlib.org/stable/api/index.html). Full Matplotlib API docs. It will be useful for the customization of the bot's plots.
- [Telegram Bot API docs](https://core.telegram.org/bots/api). Official Bot API docs provided by the Telegram.