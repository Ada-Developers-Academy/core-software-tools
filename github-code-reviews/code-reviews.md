# Code Reviews

## Introduction

Software is _usually_ not developed solo. Instead, developers work in teams and need to collaborate and share knowledge across the team. To facilitate this collaboration, teams have developed a practice known as a code review.

This document describes the general process and purpose of code reviews. In the next lesson, we will explore one method of conducting a code review using Github, known as a **pull request**.

## Our Goal

By the end of this lesson we should be able to:

- Define what a code review is
- Explain the purposes of a code review
- Write reviews with proper etiquette

## What is A Code Review?

A Code Review is a process in which one or more developers review code written by another developer as part of the quality assurance process. This is usually done before changes are merged into production and is done by reading the source code and providing comments and suggestions. The people checking and commenting are called _Reviewers_.

## Why Do Code Reviews

Code reviews provide the following benefits:

- **Readability & Consistent Style** - By ensuring that code is reviewed before it is merged into the main project, team members can ensure that the code is understandable by others beyond the author and adheres to the team's coding standards.
- **Knowledge Transfer** - When a team makes code reviews part of the development process, they ensure knowledge of each feature is shared among multiple members of the team. 
  - This minimizes disruption when a member transfers, finds new employment, retires, etc. 
  - It also makes it easier for other team members to adapt or adjust the feature under review in the future.
  - Code reviews provide a useful tool for newer team members to explore and learn about the codebase. That said, a new team member should **not** be the only reviewer.
  - Finally, code reviews allow developers to learn techniques, libraries, and tricks from other members of the team.
- **Architecture** - By involving several team members in a proposed change or feature, a code review allows the team to examine the architecture of a feature and judge it in the larger context of the application. Will the change scale?  Is it flexible and extensible? Does it match or integrate with the architecture of the larger application?
- **Finding Bugs** - As we might expect, having more eyes on code early in development allows the team to catch more bugs **before** they enter production, lowering costs and speeding up development time. 
- **Verify Against Requirements** - The team can check the submission against the requirements and verify that the code satisfies them.

<<<<<<< HEAD
=======
## Types Of Code Reviews

There are several different ways to review code.

### Pull Requests

Github and other version management software systems provide methods to review suggested changes before accepting them into the `main` branch. This is called a _Pull Request_ or PR. A PR allows team members to comment on and propose changes on a branch before it is merged in. 

### Pair Programming

Another way to provide a review on code is through _pair programming_. In pair programming, two developers work on the feature as a team. The developers take turns with one _driving_, or writing the code and focusing on the immediate task at hand. Meanwhile, the second developer _navigates_ or looks at the work from a higher level guiding around complications and obstacles the driver cannot focus on in the moment.

### Mob Programming

A third method is called [_mob programming_](https://en.wikipedia.org/wiki/Mob_programming) where a team of developers works on the same feature, at the same time, together. One developer drives while the rest of the team navigates. Mob programming can be very useful on complicated, tricky, or core features where wide understanding on the team is essential. Sometimes it is useful to have as many eyes on the code as possible.

Both mob programming and pair programming can also be done remotely using software such as [Visual Studio's Liveshare extension](https://code.visualstudio.com/blogs/2017/11/15/live-share). They also have the advantage of a very short feedback loop, while a more common pull request review happens asynchronously and can happen hours or even days later. 

>>>>>>> 7bb0067927054214251b5c2b27f5af534a1deb2f
## What to Look For In A Review

In a code review, we should be looking for:

- Edge Cases
  - Are there circumstances that will cause this code to fail unexpectedly?  
- Is the code tested adequately?
  - Is there good test coverage?
  - For areas the tests do not cover, is this a concern?
- Does it match requirements?
  - Look at the feature requirements and compare it to the code submitted. 
    - Is there anything missing from the submission or functionality not found in the requirements?
- Performance
  - Is this code efficient?
  - Did we do performance testing? Can we automate performance and load testing?
- Security
  - Are there security advisories for libraries being used?
  - Does this safeguard data adequately?

## Code Reviews Are A Discussion

As an author of a pull request, it is important to respond in a timely fashion to each actionable comment on our pull request. There may be suggestions or requests the reviewer makes that we disagree with or need more clarity on. It is important to challenge comments or suggestions that we disagree with or need more clarity on. Sometimes, the reviewer will lack the context behind a coding decision and a simple explanation from us will resolve it. If both continue to disagree, it can be helpful to get input from another team member. Remember that a code review is a discussion, not a dictated list of required changes.

## Code Review Tips for Success

- Do them!  
- Two developers will sometimes have two conflicting opinions. Get a 3rd opinion.
- Keep changes small (small branches)
- Don't trust the developer. Challenge them respectfully.
- Use your favorite tool to do code reviews. [VS Code has a PR review tool!](https://code.visualstudio.com/blogs/2018/09/10/introducing-github-pullrequests)
- Shared vision
  - Make sure the team has a shared understanding of where the application is moving and the short and long term goals. 
  - Don't review code for more than an hour. Few can stay focused that long.
  - It can be helpful to give your reviewers a checklist of things to look at.

![Code Review Meme](/assets/code-reviews/code-review-meme.jpg)

## Beyond The Code Review

There may come a time where we notice architectural issues with the application **beyond** the code being submitted in a specific PR. Maybe our app is reaching the limits of it's scalability or the application is less flexible than it could be. We may have ideas to address these issues. This is **not** something to discuss in a code review. Instead, a broader architectural exploration is something to discuss with the team lead and, if justified, we may schedule a timeboxed team meeting to present and discuss our ideas. 

## Types Of Code Reviews

There are several different ways to review code.

### Pull Requests

Github and other version management software sytems provide methods to review suggested changes before accepting them into the main branch.  This is called a _Pull Request_ or PR.  A PR allows team members to comment on and propose changes on a branch before it is merged in.  

### Pair Programming

Another way to provide a review on code is through _pair programming_.  In pair programming two developers work on the feature as a team.  The developers take turns with one _driving_, or writing the code and focusing on the immediate task at hand.  Meanwhile the second developer _navigates_ or looks at the work from a higher level guiding around complications and obsticals the driver cannot focus on in the moment.

### Mob Programming

A third method is called [_mob programming_](https://en.wikipedia.org/wiki/Mob_programming) where a team of developers works on the same feature, at the same time, together.  One developer drives while the rest of the team navigate.  Mob programming can be very useful on complicated, tricky or core features where wide understanding on the team is essential or where it is useful to have as many eyes on the code as possible.

Both mob programming and pair programming can also be done remotely using software such as [Visual Studio's Liveshare extension](https://code.visualstudio.com/blogs/2017/11/15/live-share).  They also have the advantage of a very short feedback loop, while a more common pull request review happens asynchronouslly and can happen hours or even days later.  

## Summary

Code reviews are a standard way to ensure code quality and share knowledge of the codebase. It's important to remember that a code review is a discussion between peers about the **team's** code. Like many things remembering to communicate like a human with kindness, frankness and with specificity is very helpful for a successful review. 

## Sources For This Lesson

- [The Science of Code Reviews Video](https://www.youtube.com/watch?v=EyL7mqwpZhk)
- [The Psycology of Computer Programming](https://leanpub.com/thepsychologyofcomputerprogramming) - The 1st book on the human factors of computer programming, and the 1st to mention Egoless programming.
- [Pull Request Review in VS Code](https://code.visualstudio.com/blogs/2018/09/10/introducing-github-pullrequests)
