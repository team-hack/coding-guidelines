# Code Review Guidelines

## Goals

First and foremost, we want Team Hack to be a place where all contributors feel welcome and safe. We're here to grow in our programming skills together, and that means not tearing each other down.

Tragically, code reviews can easily turn toxic and make new contributors feel unwelcome. But they don't have to be that way!

This guide consists of two main parts—both geared at making pull requests encouraging and helpful.

First, we'll look at some helpful tips for opening an amazing pull request that's a joy for others to review. Second, we'll look at some tips for reviewing a PR with empathy and compassion.

## If you're opening the PR

### Remember that you are not your code

Writing code can often be creative and fun, and as a result it's easy to feel proud of the code that you write. And you should!

When a reviewer suggests changes to some code that you wrote, try not to take it as a personal attack. We're all on the same team, and your reviewer is trying to make the codebase the best that it can be. 

### Write a PR description!

Writing a description for your PR makes it easier for reviewers to understand the _context_ behind the change that you're proposing. Chances are you've just spent some time working on a feature or a bug. As a result, you have a lot of extra context around _why_ that bug occurs in the code, what types of approaches _didn't work_, and the _trade-offs_ that you had to consider while working on the PR.

Your reviewer may not have the same amount of context as you do. Opening a PR with information helps them to better understand the changes you're proposing and makes the code review much more efficient. In addition, this helps them to provide higher-quality feedback.

Don't stress out about not including enough context or about including too much context! One good rule of thumb is to think "what information would _I_ want if I was looking at this PR" and include that in your description. If your reviewer needs more context around something, they'll ask. 😅

### If you're making a PR with UI changes, uploading a photo helps!

One cool trick when opening a PR with _UI changes_ is to also include a photo of the changes with your PR. This makes it a breeze for the reviewer to understand the effects of the styles you added/removed, since they don't need to pull the branch down and run the app themselves.

On GitHub you can attach a photo by dragging it directly into the PR description. 💪

### Small PRs are better than large PRs

Take notice of the _size_ of your PR! It's easy to get "in the zone" and have a PR get away from you. 2,000 lines later you're only halfway done. 😱

Large PRs take a more effort to review than small PRs. It may only take 5-10 minutes to review a 100-line PR, but it could easily take 45+ minutes to review a larger 1,500-line PR. This eats into your reviewer's time since they need to set aside a large chunk of time to look at the PR.

Sometimes you'll find yourself working on a big feature or refactor, and you know that it's gonna result in a big PR. One recommendation is to see if you can split that large PR into several small PRs.

For example, if you're working on adding a screen to an app but you need to refactor some code first, you can split the refactoring into one PR and then add the screen in a separate PR.

If you're planning on following up one PR with another related PR, it's always nice to include that information in the PR description. In the above example (1 refactoring PR, then adding the screen), you could drop a note in the refactoring PR that it paves the way for easily adding the screen. 🙃

Granted, there's exceptions to this guideline (some PRs just can't be sliced any smaller), but often there are ways to slice PRs smaller. It _is_ difficult and takes some practice—but it's  incredibly valuable.

### Have fun!

This isn't work! We want PRs to be something that's fun and enjoyable, not stressful and burdensome.

---

## If you're reviewing a PR

### Remember that there's a human being who wrote the PR

The person that opened this PR took time out of their busy life to contribute to open source. And it doesn't matter what the code looks like—they're a real person with feelings, emotions, hopes, and dreams. They're participating in Team Hack because they feel like it will enrich their life and enhance their career in some way.

So treat them like a person. Don't say something over the internet you wouldn't say to their face. Be respectful of their thoughts and feelings and try to give your feedback with as much empathy as you can.

### Differentiate stylistic comments from "PR blockers"

A lot of times PR feedback is purely stylistic opinions. And programmers are notorious for arguing over opinions! 😂

If you want to share your personal preferences about a bit of code, that's ok, but it's a good idea to let the PR author know that it's not something they _must_ change before the PR gets approved and merged.

For example, take the following JavaScript code:

```js
function add(a, b) {
  return a + b
}
```

Let's say you vastly prefer ES6 arrow functions. If you were writing the code, you would've done something like this:

```js
const add = (a, b) => a + b
```

Phrasing your feedback along the lines of `Not a PR-blocker, but we could use an arrow function here if we want` instead of `Use an arrow function here` lets the PR author know that it's your personal preference and not critical.

_Note: a lot of styling decisions can be automated, removing the need for most of these comments. I'm sure we'll discuss this more as a team and while setting up projects._

### Don't be overly repetitive, even if there are multiple instances that need the same feedback.

Let's say that a project _does_ have a style guide, and that style guide says that you should use semicolons for all JavaScript code.

You're reviewing a PR where the author doesn't have any semicolons in their code.

Instead of leaving 100 comments saying `Add a semicolon here`, you can just consolidate the feedback under a single comment on the PR.

```
It looks like we're missing some semicolons in this PR. Can we add them in?
```

A good rule of thumb is that if a PR needs the same comment more than 2-3 times, you can consolidate that feedback as a comment on the entire PR.

**Why is this helpful?** Every single person has an emotional "gas tank", and PR comment takes a little bit of gas out of that tank. If you pile on with the same comment 50 times, you're kicking the PR author while they're down instead of just pointing out what needs to change.

_A lot of the repetitive issues (like formatting) can be automated away with linters and formatters. A lot of modern languages have this stuff built in. That greatly reduces the situations in which a PR has tons of code requiring the exact same feedback._ 🔥

### Be respectful, not condescending

It doesn't matter whether the PR author started programming last week or 20 years ago; this isn't a place to be condescending. We're all trying to grow in our abilities together, and this should be a welcoming place. Regardless of our experience levels, we all have things that we can learn from each other.

We want this to be a safe place for people wanting to grow in their programming skills. Not somewhere that sparks anxiety and toxicity when opening a pull request.

For example, the following comments would fall into the "condescending category":

- Personal attacks on the PR author.
- Saying things like "this code is terrible" or "I hate this code"
- Being patronizing.
- Quiz-style questions in comments. Stuff like "do you know what function from `lodash` we can replace this with?" usually serves to make the commenter look good and shames the PR author if they don't know the answer. If you want to point out that there's an alternative, just say what it is.
- Saying things like "why don't we just" or "all we have to do is". This often serves to shame the PR author for not knowing that there was an alternative approach.

### Leave positive comments!

Often, reviewers only comment on the things that need to change. But positive comments are totally fine too! Feel free to leave an encouraging note or call out code that you're especially impressed by. 

## Additional resources

Here's a couple additional resources on pull requests and empathetic code reviews:

- [Become a Better Developer by Increasing Your Empathy](https://www.welcometothejungle.com/en/articles/better-developer-empathy): this isn't only about code review, but it has some great suggestions on how to make sure the tone of a review isn't toxic.
- [Google's Code Review Guidelines](https://google.github.io/eng-practices/review/): There's a wealth of good stuff in these guides for Google's code review process. _Note: Google uses "CL" (for "change list") to refer to PRs._