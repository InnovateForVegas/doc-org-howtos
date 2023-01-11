<!--
 Copyright (C) 2022 Innovate for Vegas Foundation
 
 This file is part of doc-org-howtos.
 
 doc-org-howtos is free software: you can redistribute it and/or modify
 it under the terms of the GNU General Public License as published by
 the Free Software Foundation, either version 3 of the License, or
 (at your option) any later version.
 
 doc-org-howtos is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License
 along with doc-org-howtos.  If not, see <http://www.gnu.org/licenses/>.
-->

# Issues, Bugs, and Tracking Progress

A standard tool of project management (beyond software projects) is the issue tracker, or bug database, or general backlog that can be added to, updated, and reported upon through the life of a project. If you have ever heard phrases like “open a bug” or “file a bug” or if you have ever contacted customer support and been provided an issue tracking number, these are examples of practical use. We will use the issue tracker features of GitHub, at least as far as they are useful, to keep track of issues through the life of a given project component (in a single repository) and across all components at a top level (issues assigned to the top-level ov- project overview repository is most cases).

At any given time during the life of a project or project component, it is possible to examine the total number of issues, the number opened per unit time, the number marked as closed (eg fixed or un-fixable, etc), the number waiting to be addressed, and so on, so it is possible to observe progress of any component over the life of that component (and in aggregate, the project overall). Using issue tracking rather than anecdotes (such as discussions in chat rooms or in a discord server, hidden away in email or text messages, etc), and observing these statistics, it is not so difficult to determine what sort of progress is being made, whether a project might need more people, more testing, a diversity of testing, or if there are features that simple have not been addressed at a point in time along the development timeline.

This will all figure in nicely as we develop and adopt a [Volunteer form of Agile](agile.md) (which was conceived for software developers working at companies, though we will endeavor to apply it to all project contributors volunteering their time). The Backlog, especially for User Stories, will be essential as we kick off and work on projects.

## Backlog

A *backlog* is one or more issues in the issue tracking system opened to mark work that needs to be done even before the project is started. That it, this is not necessarily a bug or problem that has been found (though those are included), but may also be a feature that does not exist but should be implemented. When working with a team of more than one person, the ability to collaborate in an organized manner is helped if the work to be done is factored into backlog items, and each member of the team works on one item at a time, marking an item as completed (ready for review) before moving to the next. The backlog list is ordered by some priority, usually placing data-loss or other critical issues at the highest.

[Wikipedia entry for Product Backlog](https://en.wikipedia.org/wiki/Product_backlog)

As part of our move to Volunteer Agile, we will make use of User Stories and a project Backlog (assigned to the overview project(s)) to specify what needs to be done, and assign the backlog tasks to individual contributors to tackle.

By using issues to track work, and by assigning issues to a particular team member (or assigning an issue to yourself to take ownership), it is possible to avoid duplicating work, losing track of who is working on which features or bugs, what the progress is, and so on. Think of the backlog as a shopping list with multiple shoppers. By splitting the list up, it is possible to shop for the items on the part of the list in hand without duplicating effort or leaving items out.

It is important to note here, that the backlog may include anything that is a part of a project effort. If there is an issue in the backlog describing the need for a set of styled icons or a logo or perhaps a language translation check, or creation of some content, or just about anything else, using this scheme for smaller teams is a completely reasonable approach to organizing forward progress whether the tasks are coding, or creating, or anywhere in between.

## History

In the GitHub scheme (and others, this it not unique to GitHub), work can begin on an issue, work progresses, the work is completed, and submitted for review. If all goes well, the issue is marked as Completed or in some cases, that the issue cannot or will not be addressed (this may mean deferring until later, or ignoring it completely). At some point in the future, it may be necessary to determine how a particular issue was addressed, and by whom, to follow up, identify potential solutions in other projects, as educational or reference material in general, or perhaps simply to attribute that contribution to the person who did the work.

Since most, if not all projects that Innovate for Vegas Foundation pursues will be ongoing and may never come to a formal end, it will always be useful to have a historical record of progress, innovation, and contribution, for all aspects of a project (not merely the code!), so that diligent use of these tools will benefit the teams working on a given project, on all projects over time (for posterity), and for your own job skills development. The ability to participate in a project management system will enable you to join a project already in progress, go through the closed items and the current backlog, and determine how the project and team are advancing, and where you can jump in and make a difference!

## Top-level Issues versus Project Component Issues

What if there is no project component (software repository or external project in Figma or Penpot or any of many potential tools, even including pencil and paper) to open an issue against? Issues, typically a part of the Backlog in this use case, should be opened for the top-level overview (ov-) repository, and copied later in the appropriate repository once one is created (or if there was some uncertainty when creating the issue initially) which can then be linked to a relevant issue created in a new component repository (which can link back) using GitHub issue linking syntax.

[GitHub Doc: Transferring Issues Between Repositories](https://docs.github.com/en/issues/tracking-your-work-with-issues/transferring-an-issue-to-another-repository)

[GitHub Doc: Issue and PR Linking](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/autolinked-references-and-urls#issues-and-pull-requests)

Why copy an issue? The Backlog issue (User Story or similar) will be a general description of what is needed, while a project component repository is the implementation of what is needed. It is entirely possible to address a top-level User Story in two different project component repositories, where each is useful under different circumstances. There are too many examples to list comprehensively, but let us take a simple example:

- Top level overview repository has a User Story in the Backlog where a User needs documentation
- In one project component, an implementation uses third-party open source elements which can be documented and discussed in a project copy of the User Story (pointing back to the overview Backlog User Story)
- In another project component, an implementation is completely stand-alone and takes a completely different approach, such that the same Backlog User Story has a different need for documentation and discussion in the project copy of the story.

The most common case of this implementation difference will come with different types of implementation using different coding languages, or graphical development tools, or any cases where a similar result addressing a Backlog User Story or other Issue is obtained in more than one way, so the project copy of the Issue allows each to progress separately while connected to the initial Backlog Issue.

*User Story* and *Issue* are used interchangeably here, the User Story is captured as an Issue in GitHub just as any feature or bug fix would be, as an Issue.

## Project Managers and Issue Tracking

One of the responsibilities of a project manager is to keep track of the issue tracker and the people filing issues, and make sure they are in the correct place (filed against the correct repository or project component), that they are useful (make sure there is enough information to enable work to be done based upon the issue), and that they are not aging (bugs never go away by themselves!). If there is a Project Manager helping out on a project, that person or team of people will be able to help determine issues with issues, and will help to keep the issues flowing from opened to closed.

It is also important to note, that not all issues will be created by the individual who needs to create the issue. Consider a normal member of the community using a My Vegas feature who finds a problem and reports it in the Innovate for Vegas Foundation Discord community server though discussion. Capturing this issue is important, because mentions and chats and anecdotes are not a part of the project progress workflow. These findings need to be converted into actual issues so that they can be found and addressed. The source of the finding (with appropriate privacy awareness) should be noted in the issue.

The role of Project Managers will be particularly interesting as we adopt Volunteer Agile, so that we can make the most of Atomic Teams and Iterations and the time and effort that goes into them.

## GitHub Projects

We are making use of the new style GitHub Project to keep track of the various component repositories that belong to a particular project. For example, the Open Transit project is used to track issues for that project across the various component repositories that are associated with that project.

As of this writing, this is a good place to begin learning about how GitHub has implemented the Issue tracking and Project management features that we will make use of for our Innovate for Vegas Foundation projects!

[GitHub Doc: Issues (and Projects)](https://docs.github.com/en/issues)
