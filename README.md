![Renpy to Itch](https://cdn.discordapp.com/attachments/1074143503262683149/1103657252457558036/renpy_to_itch_art.jpg)

# Intro

This is a Github workflow that publishes your game to Itch by pushing to specific branches. 


# Setup

- [ ] Renpy: Create your game using Renpy 8.1.
    - Versions previous to 8.1 *probably* work.

- [ ] Itch: Create a Itch.io page for your game.

- [ ] GitHub: Add the .github folder from this project to your Github repo. 
  - This repo include a .gitignore file that is not required but may be helpful if you do not already use one.

- [ ] GitHub: Fill out repo Settings->Secrets and Variables->Actions.
  - [ ] RENPY_SDK_VERSION
    - ex: 8.1.0 
    - Use 8.1.0, do not change it.
  - [ ] BUTLER_USER_SLASH_GAME
    - ex: bunnygun/dirigible-boss
  - [ ] BUTLER_API_KEY
    - ex: tD2ldJPzVAra2dkI6jJ8uZ5ziKdj3tJYLYlmKLzX

# Usage

- [ ] Push your code to 'develop', 'preview', or 'live' branch. This will trigger the workflow that will take care of building your game for various platforms, and shipping the builds to Itch.io.


# How does this work?

The work is done by the GitHub workflow file located in .github/workflows/build-and-deploy.yml.

The workflow file calls a special docker image that is preconfigured with the tools to complete the task.

The version of Renpy on the docker image is 8.1.0.

# What build types are supported?

Windows, Mac, Linux, and Web (PWA).

# License 

MIT