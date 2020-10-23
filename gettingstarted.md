# Getting Started & Next Steps

I want to just make sure everyone is on the same page by just outlining what to do next (as some people have been asking me via DM):

## Get on Discord

- Please make sure you are part of the Discord community. Here is a direct link to sign up: https://discord.gg/sFHSVR5
- Once logged in, make sure you look for the channel #teamhack on the left hand side of the channels area (the main area is where people chat).
- Click on `#teamhack` to get to the Team Hack channel and then say hello, to let us know you're in! Mission 1 complete!

## Bookmark Github

Next, after you're on Discord, be sure to also have the Github community saved (bookmarked) in your browser.

Here's the link: https://github.com/team-hack.

## Fork A Repo, Create A Feature & Submit a Pull Request

From Github, go to the repo for **coding-guidelines**. Fork this repo to your own Github by clicking the Fork button at the top right hand corner of the page.

You should see a cool animation showing the coding guidelines repo being copied to your own Github.

Now clone this repo to your local computer by selecting the **green Code button** towards middle of page and using the command:

```sh
git clone <repo url>
```

Do this inside your command line tool of choice (e.g. Terminal for Mac/Linux, Command Prompt or Powershell for Windows).

For convenience, you may want to set up a public key for yourself so you can push and pull commits without having to type in a password. It's also more secure!

After cloning the repo, go to your command line, then create a new feature branch, e.g. type:

```sh
git checkout -b "<featurebranchname>"
```

You can now open up the folder in your favorite editor, e.g. VScode or Atom, and then make some changes. We recommend making changes to the **README.md** file as it's just text (not code) so should be easy to add or change a few sentences.

When you are done, go back to your command line, then be sure to add your changes, stage and commit. Finally, push your work back to your own Github. Here are the commands you'll need:

```sh
git add --all
git commit -m "My first commit"
git push origin <featurebranchname>
```

If successful, your code should get pushed back up to your Github repo.

At the top of your own Github repo, select your feature branch from the dropdown, then you should see a new Green button in a yellow alert banner that says **Compare & pull request**. Click that button (or click Pull Request).

Next, under "Open a pull request", make sure that everything looks correct -- basically your repo should request to merge with the team-hack/coding-guidelines repo.

Under your commit message, you can write a description to further talk about what you are trying to submit. Click the **green "Create pull request"** when you are done.

Our team will review your pull request. If everything looks good we'll merge it with the "main" branch. If not, we will leave it open with comments for you to fix.

If your pull request is merged in you can now delete your feature branch and start a new feature. This is recommended as each feature branch should be associated to its own scope of work for history review.

In your terminal or command line, switch branches back to the `main` branch:

```sh
git checkout main
```

Create a reference to the upstream branch Team Hack repo in your project by going to terminal and running:

```sh
git remote add upstream https://github.com/team-hack/coding-guidelines.git
```

Pull in changes from upstream with:

```sh
git fetch upstream
git merge upstream/main
```

Your main branch should now be in sync with Team Hack's repo locally.

You can now delete your feature branch with:

```sh
git branch -d <featurebranchname>
```

Push everything so your own repo on Github is also in sync

```sh
git push
```

## Next Steps - Clone The Storybook Repo

Go back our [Team Hack main page](https://github.com/team-hack) and look for the repo `react-components`.  Go ahead and clone that down, and then start to look around the code locally on your own machine.  Be sure to create a new feature branch before doing any work.  Then see if you can edit some of the components already there or add a new component to the work if you feel confident.  We will be working to create our own component library so it's a good idea to read ahead and try to understand things before our next call.  Any questions, again ask on [Discord](https://discord.gg/sFHSVR5)!

**Any questions, please ask on Discord!!**

## Notes:

We wanted to use the JIRA boards for doing the projects, but this becomes expensive if we have more than 10 people using the board. So we are opting to use the Github Project board instead, which works almost exactly identical to JIRA. We can also refer to JIRA anytime we want to learn anything there and bring over to our project boards; so in this way we help anyone who needs help being ready to work in a JIRA environment.

Our first big project will be the components library that Ben talked about at our meeting. We will have another meeting to talk about that in more detail, but in the mean time feel free to use Discord as a place to ask questions and suggest more project ideas (especially if you want to do backend or ML or anything else).

Thanks for your support, stay safe, and see you at the next meetup!
