![Renpy to Itch](https://cdn.discordapp.com/attachments/1074143503262683149/1103657252457558036/renpy_to_itch_art.jpg)

# Intro

Welcome to this Renpy tutorial! In this video, we'll show you how to use the renpy-to-itch tool to quickly publish your Renpy games to Itch.io without the hassle of manual build uploads.

With renpy-to-itch, you can automatically build and publish your game to Itch.io for Windows, Mac, Linux, and Web (PWA) platforms. This is the perfect solution for those who want to spend less time building and publishing their games and for those who collaborate with friends locally or remotely.

So, if you're a Renpy user looking to streamline your game publishing process, this video is for you. Let's dive in!

## Setup

- For a video guide on setting up the project, [view this video](https://youtu.be/AjRrpTFw20o)

To get started with this project, follow these steps:

- [ ] Create your game using Renpy 8.1 or later versions. Although previous versions *may* work, we recommend using the latest version for the best experience.
- [ ] Create an Itch.io page for your game.
- [ ] Add the `.github` folder from this project to your GitHub repository. The `.gitignore` file included in this repo is optional, but it can be helpful if you don't already have one.
- [ ] In your GitHub repo, go to Settings > Secrets and Variables > Actions, and fill out the following:
  - [ ] `BUTLER_USER_SLASH_GAME`: Enter your Itch.io user name followed by a forward slash (`/`) and your game's URL slug. For example: `bunnygun/dirigible-boss`
  - [ ] `BUTLER_API_KEY`: Enter your Itch.io API key. You can find this in your Itch.io account settings.

## Usage

To use this project, simply push your code to the `develop`, `preview`, or `live` branch in your GitHub repository. This will trigger the workflow that will build your game for various platforms and automatically ship the builds to Itch.io.

## How does this work?

The heavy lifting is done by the GitHub workflow file located in `.github/workflows/build-and-deploy.yml`. This workflow file calls a preconfigured Docker image that includes all the necessary tools to complete the task. The Renpy version on the Docker image is 8.1.0.

## What build types are supported?

This project supports building games for Windows, Mac, Linux, and Web (PWA) platforms.

## License 

This project is licensed under the MIT License.
