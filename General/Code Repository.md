# Code Repository
Best practices related to code management

Table of Content
*  [Commit Messages](#commit-messages)
*  [Pull Request](#pull-request)
*  [Learn Git](#learn-git)

## Commit Messages
Write good commit messages, your future self and your team mates will thank you later. Good thing is that we don't need to debate on defining what is a "Good Commit Message", its already defined: [Conventional Commit](https://www.conventionalcommits.org/en/v1.0.0-beta.4/), and has plenty of advangtages including change logs and versioning. There exist tools in every language to incorporate (and enforce) these commit messages in your daily routine. For example you can use [this for Node](https://www.npmjs.com/package/commitizen) and [this for Python](https://woile.github.io/commitizen/).

Each commit **should be** associated with a ticket in your ticket management system and changes in the commit message should be relevant to that ticket only. This approach encourages you to breakdown your work into smaller units and commit frequently.

In short, unless you are working on a quick and dirty prototype, **you must**
 - Write code against a logged ticket
 - Follow Conventional Commit guideline to write your commit message
 - Refer the ticket in your commit message

## Pull Request
There is one and only one way to merge your changes into an upstream branch and that is through a **Pull Request**, period. This has multitude of advantages

 - It enforces the process of code reviews
 - Clean and meaningful git history (using merging and squashing)
 - You can associate a lot of tooling with pull requests in order to catch the problems early, on creator's side, before it reaches the reviewer.

It is important to keep in mind

 - If your team is not already in the habit of doing PR based development, at the start it might seem overhead but once you get used to it, you will never look back.
 - As a team lead or senior developer it is important for you to attend to PRs as soon as possible to ensure people don't get blocked due PR based workflow.

## Learn Git
You will use Git, (almost) daily, for rest of your programming life. And **it is wise to have a deep, friendly, and mutually respectful relationship with someone you are going to interact with daily, to successfully go through the lows and the highs**. (were you expecting this wisdom in a programming manual? you are welcome).

Git is a data structure. It's a Directed Acyclic Graph (or DAG) to be specific. It is worth understanding what that means because it will give you a visual model and a way to think while using Git. As a result you will be more effective.

There is no point in going into the details of Git and DAG, you will file plenty of them on the internet, like [this one](https://hackernoon.com/understanding-git-branching-2662f5882f9).
