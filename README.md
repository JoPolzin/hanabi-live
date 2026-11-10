<!-- markdownlint-disable MD041 -->

<p align="center">
  <img src="https://github.com/Hanabi-Live/hanabi-live/raw/main/public/img/logos/2.png" height=200 alt="Logo" title="Logo">
</p>

<br>

## Description

- **This is a fork before [upstream](https://github.com/Hanabi-Live/hanabi-live) started pushing too many changes, which are (presumably) AI slop.** 
- It is the source code for [Hanab Live](http://hanab.live/), a website that allows people to play a cooperative card game online. It is similar to the card game [Hanabi](https://boardgamegeek.com/boardgame/98778/hanabi).
- This project has no affiliation with the card game Hanabi, [Antoine Bauza](https://en.wikipedia.org/wiki/Antoine_Bauza) (the creator of Hanabi), or any of the the real-life publishers of the game (of which there are many).
- The client is programmed in [TypeScript](https://www.typescriptlang.org/). It is located in the [`packages/client`](packages/client) directory.
  - A lot of the code was originally taken from [Keldon Jones'](http://keldon.net/) implementation of the game. (His site no longer exists.)
- The server is programmed in [Go](https://golang.org/). It is located in the [`server`](server) subdirectory.
  - It uses a [PostgreSQL](https://www.postgresql.org/) database to store information about the users and games.
- The core game logic is located in the [`packages/game`](packages/game) directory.

## Discord

Find teammates to play games with at [the Discord server](https://discord.gg/FADvkJp). We also discuss code changes here. Note that this is the discord server of **upstream** so not specific to this fork.

## List of Variants and Features

Hanab Live is different from normal Hanabi in that it implements [many special variants](docs/variants.md), in which the rules are changed to make the game more difficult.

Also, see the [features documentation](docs/features.md).

## Deployment

Deployment is only supported via the docker image. To set it up, you'll need the following two images which are published on `ghcr` and built from main by CI:
- The actual server: `ghcr.io/jopolzin/hanabi-live:main`
- The database with schema: `ghcr.io/jopolzin/hanabi-live-db:main`

To deploy it, take a look at the [docker compose file](docker-compose.yml) in this repository for an example to work off of!

For more generic instructions and how to set up a development setup, see the [installation documentation](docs/install.md).

## Credits

- [Antoine Bauza](https://en.wikipedia.org/wiki/Antoine_Bauza) created Hanabi, which was the inspiration for this website. If you enjoy playing online, then you should purchase a physical copy of the game, since he will presumably receive a portion of the proceeds.
- [Keldon Jones](http://keldon.net/) was the original creator of the slick client-side user interface.
- [Hyphen-ated](https://github.com/Hyphen-ated/) coded many useful add-on features for Keldon's site that are integrated into Hanab Live.
