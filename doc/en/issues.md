<!--
 Copyright (C) 2022 Innovate for Vegas Foundation
 
 This file is part of doc-cfv-howtos.
 
 doc-cfv-howtos is free software: you can redistribute it and/or modify
 it under the terms of the GNU General Public License as published by
 the Free Software Foundation, either version 3 of the License, or
 (at your option) any later version.
 
 doc-cfv-howtos is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License
 along with doc-cfv-howtos.  If not, see <http://www.gnu.org/licenses/>.
-->

# Issues, Bugs, and Tracking Progress

A standard tool of project management (beyond software projects) is the issue tracker, or bug database, or general backlog that can be added to, updated, and reported upon through the life of a project. If you have ever heard phrases like “open a bug” or “file a bug” or if you have ever contacted customer support and been provided an issue tracking number, these are examples of practical use. We will use the issue tracker features of GitHub, at least as far as they are useful, to keep track of issues through the life of a given project component (in a single repository) and across all components at a top level (issues assigned to the top-level ov- project overview repository is most cases).

At any given time during the life of a project or project component, it is possible to examine the total number of issues, the number opened per unit time, the number marked as closed (eg fixed or unfixable, etc), the number waiting to be addressed, and so on, so it is possible to observe progress of any component over the life of that component (and in aggregate, the project overall). Using issue tracking rather than anecdotes (such as discussions in chat rooms or in a discord server, hidden away in email or text messages, etc), and observing these statistics, it is not so difficult to determine what sort of progress is being made, whether a project might need more people, more testing, a diversity of testing, or if there are features that simple have not been addressed at a point in time along the development timeline.

## Backlog

A *backlog* is one or more issues in the issue tracking system opened to mark work that needs to be done before it is started. That it, this is not necessarily a bug or problem that has been found (though those are included), but may also be a feature that does not exist but should be implemented. When working with a team of more than one person, the ability to collaborate in an organized manner is helped if the work to be done is factored into backlog items, and each member of the team works on one item at a time, marking an item as completed (ready for review) before moving to the next. The backlog list is ordered by some priority, usually placing data-loss or other critical issues at the highest.

[Wikipedia entry for Product Backlog](https://en.wikipedia.org/wiki/Product_backlog)

By using issues to track work, and by assigning issues to a particular team member (or assigning an issue to yourself to take ownership), it is possible to avoid duplicating work, losing track of who is working on which features or bugs, what the progress is, and so on. Think of the backlog as a shopping list with multiple shoppers. By splitting the list up, it is possible to shop for the items on the part of the list in hand without duplicating effort or leaving items out.

It is important to note here, that the backlog may include anything that is a part of a project effort. If there is an issue in the backlog describing the need for a set of styled icons or a logo or perhaps a language translation check, or creation of some content, or just about anything else, using this scheme for smaller teams is a completely reasonable approach to organizing forward progress whether the tasks are coding, or creating, or anywhere in between.

## History

In the GitHub scheme, work can begin on an issue, work progresses, the work is completed, and submitted for review. If all goes well, the issue is marked as Completed or in some cases, that the issue cannot or will not be addressed (this may mean deferring until later, or ignoring it completely). At some point in the future, it may be necessary to determine how a particular issue was addressed, and by whom, to follow up, identify potential solutions in other projects, as educational or reference material in general, or perhaps simply to attribute that contribution to the person who did the work.

Since almost all projects that Innovate for Vegas Foundation will pursue will be ongoing and may never come to a formal end, it will always be useful to have a historical record of progress, innovation, and contribution, for all aspects of a project (not merely the code!), so that diligent use of these tools will benefit the teams working on a given project, on all projects over time (for posterity), and for your own job skills development. The ability to participate in a project management system will enable you to join a project already in progress, go through the closed items and the current backlog, and determine how the project and team are advancing, and where you can jump in and make a difference!

## Top-level Issues

What if there is no project component (software repository or external project in Figma or Penpot or any of many potential tools, even including pencil and paper) to open an issue against? GitHub issues may be moved between repositories, which means if there is not yet a suitable component repository, an issue may be opened for the top-level overview (ov-) repository, and moved later to the appropriate repository once one is created (or if there was some uncertainty when creating the issue initially) or, even better, linked to a relevant issue created in a new component repository (which can link back) using GitHub issue linking syntax.

[GitHub Doc: Transferring Issues Between Repositories](https://docs.github.com/en/issues/tracking-your-work-with-issues/transferring-an-issue-to-another-repository)

[GitHub Doc: Issue and PR Linking](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/autolinked-references-and-urls#issues-and-pull-requests)

## Project Managers and Issue Tracking

One of the responsibilities of a project manager is to keep track of the issue tracker and the people filing issues, and make sure they are in the correct place (filed against the correct repository or project component), that they are useful (make sure there is enough information to enable work to be done based upon the issue), and that they are not aging (bugs never go away by themselves!). If there is a Project Manager helping out on a project, that person or team of people will be able to help determine issues with issues, and will help to keep the issues flowing from opened to closed.

It is also important to note, that not all issues will be created by the individual who needs to create the issue. Consider a normal member of the community using a My Vegas feature who finds a problem and reports it in the Innovate for Vegas Foundation Discord community server though discussion. Capturing this issue is important, because mentions and chats and anecdotes are not a part of the project progress workflow. These findings need to be converted into actual issues so that they can be found and addressed. The source of the finding (with appropriate privacy awareness) should be noted in the issue.

## GitHub Projects

We are making use of the new style GitHub Project to keep track of the various component repositories that belong to a particular project. For example, the Open Transit project is used to track issues for that project across the various component repositories that are associated with that project.

As of this writing, this is a good place to begin learning about how GitHub has implemented the Issue tracking and Project management features that we will make use of for our Innovate for Vegas Foundation projects!

[GitHub Doc: Issues (and Projects)](https://docs.github.com/en/issues)
