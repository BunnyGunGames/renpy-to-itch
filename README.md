![Renpy to Itch](https://cdn.discordapp.com/attachments/1074143503262683149/1103657252457558036/renpy_to_itch_art.jpg)

# Intro

This is a Github workflow that publishes your game to Itch by pushing to specific branches. 


# Setup

- For a quick start guide for new projects, [try this video](https://youtu.be/BycnOyOdSxw).
- For a video guide on setting up existing projects, [try this video](https://youtu.be/AjRrpTFw20o)


- [ ] Renpy: Create your game using Renpy 8.1.
    - Versions previous to 8.1 *probably* work.

- [ ] Itch: Create a Itch.io page for your game.

- [ ] GitHub: Add the .github folder from this project to your Github repo. 
  - This repo includes a .gitignore file that is not required but may be helpful if you do not already use one.

- [ ] GitHub: Fill out repo Settings->Secrets and Variables->Actions.
  - [ ] BUTLER_USER_SLASH_GAME
    - ex: bunnygun/dirigible-boss
  - [ ] BUTLER_API_KEY
    - ex: tD2ldJPzVAra2dkI6jJ8uZ5ziKdj3tJYLYlmKLzX

# Usage

To use this project, simply push your code to the develop, preview, or live branch in your GitHub repository. This will trigger the workflow that will build your game for various platforms and automatically ship the builds to Itch.io.


# How does this work?

The heavy lifting is done by the GitHub workflow file located in .github/workflows/build-and-deploy.yml. This workflow file calls a preconfigured Docker image that includes all the necessary tools to complete the task. The Renpy version on the Docker image is 8.1.0.

# What build types are supported?

This project supports building games for Windows, Mac, Linux, and Web (PWA) platforms.

# License 

This project is licensed under the MIT License.
