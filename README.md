# `git-fire` :fire:

### ![Inspiration](https://i.imgur.com/3POtveC.jpg)

`git-fire` is a Git plugin that **helps in the event of an emergency** by switching to the repository's root directory, adding all current files, committing, and pushing commits and all stashes to a new branch (to prevent merge conflicts).

**Alias it to [`git out`](https://np.reddit.com/r/ProgrammerHumor/comments/3nc531/in_case_of_fire/cvmxnv1) or [`git going`](https://np.reddit.com/r/ProgrammerHumor/comments/3nc531/in_case_of_fire/cvmsajb) for comedic effect.**

- `git config --global alias.out fire`
- `git config --global alias.going fire`

## What It Does

- changes directory to root directory of the repository
- creates new branch `fire-<current branch>-<user email>-<current epoch>`
- adds all files
- commits with `"Fire! Branch <new branch>"` or custom message
- pushes commits to remote
- pushes all stashes to remote

## Usage

`git-fire <message>`

`<message>` is optional. If not specified, `"Fire! Branch fire-<current branch>-<user email>-<current epoch>"` will be used.

## Installation

Just copy `git-fire` to your `$PATH` and ensure it is an executable (`chmod +x git-fire`) and you're good to go. 👍

`git-fire` is also installable via [NPM](https://npmjs.com/git-fire). Just run `npm install -g git-fire`, which will copy the `git-fire` binary to your `$PATH`.

Also make sure you have Git installed.

## Credit

Originally seen on [Hackathon Hackers Facebook](https://www.facebook.com/groups/hackathonhackers) group.

[Original Reddit post](https://www.reddit.com/r/ProgrammerHumor/comments/3nc531/in_case_of_fire/)

[Image source](https://instagram.com/p/8N8J8wRgPq/) | [Printable Image](http://imgur.com/IiAdxbB) | Artist: [Ákos Szokodi](https://github.com/szokodiakos)
