# Gitflow Explanation

Gitflow is a pattern of branch management that you can use on a repo, provided that you are using the continuous delivery mindset, which means that you are continuously adding new code to your production environment, usually on a schedule. One way to prevent buggy code or partial features (ie a feature has 7 tickets but only 4 are complete and merged to the develop branch when it's time to release to production) is to put those features behind a feature flag and keep the feature flag turned off on production until all the tickets are completed. This allows you to continuously deliver partial code and turn it on only when the the whole feature is complete.

Here's a link with the "traditional" [explanation of gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow
). It's a lot of words and pretty pictures but is still a little confusing because it's so long. The following is a brief explanation of how I've seen gitflow used that's a little simpler to understand.

## 2 long-lived branches

There are 2 long-lived branches: `main` and `develop`. Main is a copy of the code that is on production, develop is all the features and bugfixes that are ready to go to production. These 2 branches are usually protected by rules on the repository so that no one can push directly to these branches. The only way code gets to these branches is by opening a pull request from one of the 4 types of branches below.

## 4 types of branches

There are 4 types of branches that you create in this workflow:

1. feature
2. bug
3. release
4. hotfix

A feature branch is a branch that's created from the long-lived `develop` branch and is where you put code for new features that you're creating. Typically named something like: `feature/<ticket-number>/<short-description-of-feature>`

A bug branch is a branch that's created from the long-lived `develop` branch and is where you put code that fixes low-priority bugs, which are bugs that you can wait until your next scheduled production release to fix. Typically named something like: `bug/<ticket-number>/<short-description-of-bug>`

A release branch is a branch that's created from the long-lived `develop` branch and is where the features and bugfixes that are ready to go to production are moved in preparation to be released to production. Generally the code on a release branch goes to a qa/staging/pre-production environment (there's differing names for this environment at different companies/organizations) for testing and once tests are passed the release branch can be merged to main** and the production code updated with the new features and bugfixes. Typically named something like: `release/<version-number>`

A hotfix branch is a branch that's created from the long-lived `main` branch and is used to fix high-priority bugs that can't wait for the next production release. This branch is usually put on a qa/staging/pre-production environment for testing and once tests are passed can be merged to main** and the production code updated with the fix. Typically named something like: `hotfix/<ticket-number>/<short-description-of-bug>`

** After you merge the release or hotfix branch to main typically you will then do a merge of the main branch back to the develop branch to keep the two branches in sync.

That's the whole gist of gitflow. We can talk for days about justifications for it and modifications that various organizations use, but that's the basic mechanics of it, in case anyone ever asks you.
