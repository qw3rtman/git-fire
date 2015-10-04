# `git-fire` 🔥

### ![Inspiration](https://i.imgur.com/3POtveC.jpg)

`git-fire` is a Git plugin that **helps in the event of an emergency** by adding all current files, committing, and pushing to a new branch (to prevent merge conflicts).

**Alias it to [`git out`](https://np.reddit.com/r/ProgrammerHumor/comments/3nc531/in_case_of_fire/cvmxnv1) or [`git going`](https://np.reddit.com/r/ProgrammerHumor/comments/3nc531/in_case_of_fire/cvmsajb) for comedic effect.**

## What It Does

- creates new branch `fire-<current branch>-<user email>-<current epoch>`
- adds all files
- commits with `"Fire! Branch <new branch>"` or custom message
- pushes to remote

## Usage

`git-fire <message>`

`<message>` is optional. If not specified, `"Fire! Branch fire-<current branch>-<user email>-<current epoch>"` will be used.

## Installation

Just copy `git-fire` to your `$PATH` and ensure it is an executable (`chmod +x git-fire`) and you're good to go. 👍

Also make sure you have Git installed.

## Credit

Originally seen on [Hackathon Hackers Facebook](https://www.facebook.com/groups/hackathonhackers) group.

[Original Reddit post](https://www.reddit.com/r/ProgrammerHumor/comments/3nc531/in_case_of_fire/)
