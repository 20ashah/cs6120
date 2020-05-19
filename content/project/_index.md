+++
title = "Projects"
+++
# Language Implementation Projects

There are several implementation projects in this course.
Here’s what you do for each one:

* Propose a project and submit a short description of your plan.
* Implement something, according to the project description.
* Measure your implementation empirically and draw rigorous conclusions. (Negative results are OK! But flimsy evaluation is not.)
* Write a report as a post on our [course blog][blog].
* Do an in-class design review to collect feedback from your peers.

You can work in a small team if you want—up to about 3 people.
You are also totally welcome to work alone.

[blog]: @/blog/_index.md


## Projects

There are four projects:

1. [Make Something Cool for Bril.][p1]
2. [Implement an Optimization.][p2]
3. [Write an LLVM Pass.][p3]
4. [Implement Something.][p4]

[p1]: @/project/1.md
[p2]: @/project/2.md
[p3]: @/project/3.md
[p4]: @/project/4.md


## Proposal

At the beginning of the project period, you will decide what to do for the project.
Each project has guidelines for in-scope projects and will include a list of ideas, but you can also pick your own.
It is possible to pick the same idea as someone else in the course—these projects are open ended enough that you will inevitable end up taking the idea in a different direction, and comparing your strategies might end up being interesting.

To propose a project, [open a GitHub issue][proposal] answering these three questions, which are a sort of abbreviated form of the [Heilmeier catechism][hc]:

* What will you do?
* How will you do it?
* How will you empirically measure success?

You only need a single sentence per question, but you can of course write more if you need to.
The instructor may have feedback for your or just tacitly approve your idea.

[hc]: https://www.darpa.mil/work-with-us/heilmeier-catechism
[proposal]: https://github.com/sampsyo/cs6120/issues/new?labels=proposal&template=project-proposal.md&title=Project+%5BNUMBER%5D+Proposal%3A+%5BTITLE%5D


## Implementation

The main phase, of course, is implementing the thing you said you would implement.
I recommend you keep a “lab notebook” to log your thoughts, attempts, and frustrations—this will come in handy for the report you'll write about the project.

I strongly recommend that you develop your code as an open-source project.
Use a publicly-visible version control repository on a host like GitHub, and include an [open source license][osi].
When you create your repository, comment on your proposal GitHub issue with a link.
(If you have a specific objection to open-sourcing your code, that's OK—include a description of how you'll share your code privately with me.)

You can build on previous projects (by yourself or others in the course) and other existing implementations to do your project—unless
you’re doing something very similar to someone else in the course, in which case you can’t use their code.
(You will need to be totally clear about what you did and did not do yourself.)

[osi]: https://opensource.org/licenses


## Evaluation

A major part of your project is an empirical evaluation.
To design your evaluation strategy, you will need to consider at least these things:

* Where will you get the input code you'll use in your evaluation?
* How will you check the correctness of your implementation?
  If you've implemented an optimization, for example, “correctness” means that the transformed programs behave the same way as the original programs.
* How will you measure the benefit (in performance, energy, complexity, etc.) of your implementation?
* How will you present the data you collect from your empirical evaluation?

Other questions may be relevant depending on the project you choose.
Consider the [SIGPLAN empirical evaluation guidelines][eeg] when you design your methodology.

[eeg]: https://www.sigplan.org/Resources/EmpiricalEvaluation/


## Report

For the main project deadline, you will write up the project’s outcomes in the form of a post on the [course blog][blog].
Your writeup should answer these questions in excruciating, exhaustive detail:

* What was the goal?
* What did you do? (Include both the design and the implementation.)
* What were the hardest parts to get right?
* Were you successful? (Report rigorously on your empirical evaluation.)

To submit your report, open a pull request in [the course’s GitHub repository][gh] to add your post to the blog.
In your PR description, please include “closes #N” where N is the issue number for your proposal.
The repository README has instructions.

[gh]: https://github.com/sampsyo/cs6120


## Design Review

The culmination of a project is an in-class design review.
You'll describe your idea, implementation decisions, and measurements to the rest of the class.
The point is less about informing us about what you did and more about facilitating a discussion to get critical opinions from your peers.
Based on the feedback you get, you may optionally decide to improve your implementation or report.
(Your grade will incorporate the improvements you make.)
