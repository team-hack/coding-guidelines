# Github Coding Guidelines

As you may be aware, Github is tackling the subject of #blacklivesmatter.  An impact of this is the change of pushing to a `master` repo to now a `main` repo.

In a nutshell, the **master** terminology conjures the relationship between a master and a slave, and so to be culturally sensitive -- the term "master" is being phased out.

## What Do YOU Need To Do?

When starting a project on Github, you may notice that the default branch is "main", not "master".

If you create files locally and then commit them to a `master` branch, you may notice that your branch is different from the `origin`.  If you push to `origin/master`, you will end up with two branches rather than your changes going to the default branch.

### Before Pushing Changes, Create Branch Main, Delete Master

Here's how to fix your workflow.  NOTE: Before you make this fix, be sure you have committed all changes to your `master` branch (including any Pull Requests) otherwise those changes will be deleted / closed.

```
git log --oneline
```

You'll see a print out of where your HEAD currently points to. Something like this:

```
dfa590e (HEAD -> master, origin/master, origin/HEAD) Change text
8c46e9e Add Github button
```

Notice how the HEAD and origin both point to a "master".  We'll want to change that by creating a new branch called `main` like so:

```
git checkout -b main
```

After doing this you should see `Switched to a new branch 'main'`.

Next, do a `git log --oneline`.  You should see output like:

```
dfa590e (HEAD -> main, origin/master, origin/HEAD, master) Change text
8c46e9e Add Github button
```

Notice how HEAD now points to main, origin/master, origin/HEAD and master.

Next, if your project on Github is "defaulting" to master, you'll want to go to the project settings for the repo, by clicking **Settings** > **Branches**, and then updating the Default branch from `master` to `main`.   Doing so will now make `main` the default page when someone visits your Github repository.

Let's finish up by deleting the master branch locally on our computer:

Note: Be sure you are on the `main` branch with `git branch` and check with the command `git log --oneline --graph --decorate --all` that the `origin/master` is in a red color, indicating the next push will remove the reference.

Use:

```
git branch -d :master
```

The `:` sign in front of a branch says delete the branch listed remotely.

