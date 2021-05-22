# Getting Started & Next Steps

I want to just make sure everyone is on the same page by just outlining what to do next (as some people have been asking me via DM):

## Get on Discord

- Please make sure you are part of the Discord community. Here is a direct link to sign up: https://discord.gg/cZaysF33Ge
- Once logged in, make sure you look for the channel #teamhack on the left hand side of the channels area (the main area is where people chat).
- Click on `#teamhack` to get to the Team Hack channel and then say hello, to let us know you're in! Mission 1 complete!

## Bookmark Github

Next, after you're on Discord, be sure to also have the Github community saved (bookmarked) in your browser.

Here's the link: https://github.com/team-hack.

## Create A Feature & Do Work, And Keep Up To Date With Origin

Clone a repo to your local computer by selecting the **green Code button** towards middle of page and using the command:

```sh
git clone <repo url>
```

> Anything in angular brackets `<>` syntax means placeholder and you should write your own appropriate text, e.g. here get the real repo url and plug it in the place of the `<repo url>`.

Do this inside your command line tool of choice (e.g. Terminal for Mac/Linux, Command Prompt or Powershell for Windows).

For convenience, you may want to set up a public key for yourself so you can push and pull commits without having to type in a password. It's also more secure! Some good documentation on [setting up Git and SSH can be found via this link](https://gorails.com/setup/osx/11.0-big-sur).

After cloning the repo, go to your command line, then create a new feature branch, using the following syntax:

```sh
git checkout -b feature/<issue>/<issue-name>
```

An example could be: `git checkout -b feature/issue-<number>/typescript-support`. (If a number is relevant, please add it to the issue).

> Keep your branch names short and concise please.

You can now open up the folder in your favorite editor, e.g. VScode or Atom, and then make some changes. Feel free to look through git history as well to get a sense of what's been in development, and ask questions about anything you don't understand via Discord or issues. Make changes as you see fit to fix the issue, and then push up.

To push up, go back to your command line, add your changes to stage, then commit. Be sure to first pull down from the project main branch (usually `main` or `develop` -- check the project) and work on any merge conflicts before pushing your work. Typically, if I haven't made any local commits yet, I'll just stash my work and then apply my changes after pulling from the project main branch.

```sh
git stash
git fetch origin <project main branch name>
git merge <project main branch name>
git stash apply
```

> If there were changes to the feature branch as well, you'll want to fetch and merge those changes as well -- e.g. if you are working with another programmer on the same feature.

> You can use `git pull` as a shortcut to `git fetch` and `git merge`, but be sure to set up your tracking if you want this convenience.

If you do make commits locally, and then pull from the origin -- you might get **merge conflicts**. That's okay, just go through each file with a mergetool (I like VSCode) and update the code appropriately before making a new commit to push up. You may also have no merge conflicts and just be asked to make a new commit automatically.

Finally, push your work. Here are the commands you'll need:

```sh
git add --all
git commit -m "My first commit"
git push origin feature/<issue-number>/<issue-name>
```

If successful, your code should get pushed back the Github repo you've cloned from.

## Make a Pull Request

At the top of the Github repo, you should see a new Green button in a yellow alert banner that says **Compare & pull request**. Click that button (or click Pull Request).

Next, under "Open a pull request", make sure that everything looks correct -- basically your repo should request to merge with active Team Hack branch.

Under your commit message, you can write a description to further talk about what you are trying to submit. Github supports screenshots as well if you need to show pictures.

The next step is for your code to build, since we support a CI/CD workflow -- aka Continous Integration and Continuous Development. We'll either have Travis or Github Actions installed for the project, which will build your code and check the following:

1. Your code is linted
2. You've written tests and they pass
3. Additional rules as necessary for project

If your code fails, you'll need to fix these errors locally before submitting another PR (pull request). If you need help, ask for help on our Discord channel and get a pair partner to help you figure out what's going on.

You can and should request code reviews too -- since you'll need at least one other person (besides yourself) to review and approve the code. Once code builds and is approved, you can merge it to our active branch.

If your pull request is merged in you can now delete your feature branch and start working on another feature / issue. This is recommended as each feature branch should be associated to its own scope of work for history review.

## Next Steps - Show Us You Understand

Clone this repo, and your **first issue will be to help make sure this document is up to date.**

Create a feature branch using the commands you read above with the following branch syntax:

```sh
git checkout -b feature/update-readme/<my-update-summary>
```

Make any changes you see fit, and then push back up and submit a pull request. Then let us know on Discord and get someone to give you an approval. You won't need to worry about linting / tests with this repo, but when you work on the next project -- that's when you'll need to also make sure your build passes.

Here's the link to [Discord](https://discord.gg/sFHSVR5) again.

🚀 Good luck!
