# Github Pull Requests

In this section we will walk through the code review process using Github pull requests. Git is the most common version control system and Github the largest hosting service for git repositories. Thus, Github makes a good starting point for practicing code reviews.  

Much of the steps and etiquite of a code review apply across systems.

## Our Goal

By the end of this lesson we should be able to:

- Use Github Pull Requests to provide feedback on a code review

## The Mechanics of a Github PR Review

### Requesting a PR

As you begin working on a feature, [start the feature on a branch](https://www.git-tower.com/learn/git/faq/create-branch). It is also a good idea to check and make sure you are using linters and tools to help enforce your team's adopted style guide. This will prevent stylelistic errors and help reviewers focus on what the code is doing. You should also try to keep the changes as small and focused as possible. It is much easier for reviewers to understand and evaluate changes when they are of modest size.

Before you make a pull request make sure that:

1. The code compiles/executes successfully
1. The code is adequately tested
1. You have examined the changes yourself one final time.

When your feature is ready, push all changes up to Github:

```bash
$ git push origin <BRANCH_NAME>
```

Then go to Github and find your branch and click on the `New Pull Request` button.

![New Pull Request Button](/assets/code-reviews/new-pull-request.png)

Then add a description to your PR describing the feature and rationale for the changes.  Communicate the changes clearly.  Add any open questions you still have about the feature.  Then you can use gear icon under reviewers to request a code review.

![Request Code Review](/assets/code-reviews/request-reviewers.png)

### Reviewing Code in Github

To review a pull request on the github webpage first click on the `files changed` tab.  

![files changed tab](/assets/code-reviews/files-changed.png)

Then you can examine the proposed changes.  You can click on a `+` sign next to any line of code to add inline comments.  The comments are in [markdown](https://guides.github.com/features/mastering-markdown/) format.  

Code review comments may include:

- Questions to the author about the purpose or need for the code.
- Suggestions for improvements
- Compliments

It is important to remember that the code belongs to the team. Use the word "We" over "You". Feel free to criticize the code, while being respectful of the author.  **Be specific** in your comments or questions. You can add code samples to illustrate your point. Remember that your comments in a code review are **suggestions** and not commands.  

When you have finished reviewing the PR, click on the `Review Changes` button and leave a summary of your impressions. Either **approve** or **request changes** for the review.

![Review Changes Button and summary textbox](/assets/code-reviews/review-changes.png)
