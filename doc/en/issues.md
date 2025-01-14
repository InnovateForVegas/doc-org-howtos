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

A standard tool of project management (beyond software projects, but definitely regarding software projects) in any industry is the issue tracker, or bug database, or general backlog that can be added to, updated, and reported upon through the life of a project. If you have ever heard phrases like “open a ticket” or “file a bug” or if you have ever contacted customer support and been provided an issue tracking number, these are examples of practical use. We use the issue tracker features of GitHub, at least as far as they are useful, to keep track of issues through the life of a given Entity, whether an Initiative, Component Project, or something else.

Note that for consistency, we refer to Initiatives as a top-level effort with zero or more Component Projects attached, all of these are referred to generally as Entities and may refer to Software elements specifically, or to other elements that are not stored as software source files in repositories. The Repositories for all Entities are used to keep track of relevant information, tasks as issues, stories as issues, and so on. The classic role, “Project Manager,” will be used but keep in mind we are referring to Entities, Initiatives, Component Projects, Agile for Volunteers issues, and so on, and the coordination and oversight of these.

This will all figure in nicely as we develop and adopt [Agile for Volunteers](agile.md) (Note that Agile itself was conceived for software developers working at companies, we endeavor to apply it to all contributors volunteering their time, effort, and expertise). The Backlog, especially for Features and User Stories, but also for their associated Tasks, will be essential as we pursue Volunteer Contributions of time, effort, and expertise to any Entities.

## Backlog

A *backlog* is one or more issues in the issue tracking system opened to mark work that needs to be done even before the project is started. That it, this is not necessarily a bug or problem that has been found (though those are included), but may also be a feature or more specific user story that does not exist but should be implemented. When working with a team of more than one person, the ability to collaborate in an organized manner is helped if the work to be done is factored into backlog items, and each member of the team works on one item at a time, marking an item as completed (ready for review) before moving to the next. The backlog list is ordered by some priority, usually placing data-loss or other critical defect issues at the highest.

[Wikipedia entry for Product Backlog](https://en.wikipedia.org/wiki/Product_backlog)

As part of our move to Agile for Volunteers, we will make use of the Feature and User Story hierarchy and a project Backlog (assigned to the overview project(s)) to specify what needs to be done, and create the backlog tasks themselves within individual Component Projects assigned to contributors to tackle.

By using issues to track plans and tasks, and by assigning issues to a particular team member (or assigning an issue to yourself to take ownership), we endeavor to avoid duplicating work, losing track of who is working on which features or defects, what the progress is for each, and so on. Think of the backlog as a shopping list with multiple shoppers. By factoring this list into achievable units of effort, it is possible to shop for the items on the part of the list in hand without duplicating effort or forgetting items. AS well it makes the task of attributing effort to individual volunteer contributors a bit easier, and that is important.

The backlog may include anything that is a part of an Initiative effort. If there is an issue in the backlog describing the need for a set of styled icons or a logo or perhaps a language translation check, or creation of some content, or just about anything else, using this scheme for smaller teams is a completely reasonable approach to organizing forward progress whether the tasks are coding, or creating, or anywhere in between.

## History

In the GitHub scheme (and with other similar tools, this it not unique to GitHub), work can begin on an issue, work progresses, the work is completed, and submitted for review. If all goes well, the issue is marked as Completed or in some cases, that the issue cannot or will not be addressed (this may mean deferring until later, or ignoring it completely). At some point in the future, it may be necessary to determine how a particular issue was addressed, and by whom, to identify potential solutions in other entities, as educational or reference material in general, or perhaps simply to attribute that contribution to the person who contributed the work.

Since most, if not all Initiatives that Innovate for Vegas Foundation pursues will be ongoing and may never come to a formal end (that is, there is no specific End of Life for any particular Initiative as of this writing, this is subject to change for any particular Initiative existing or added in the future), it will always be useful to have a historical record of progress, innovation, and contribution, for all aspects of an Initiative (not merely the code!), so that diligent use of these tools will benefit the teams working on a given Initiative, on all Component Projects over time (for posterity), and for one´s own job skills development. The ability to participate in collaborative development via a project management system will enable you to join a project already in progress, go through the closed items and the current backlog, and determine how the project and team are advancing, and where you can jump in and make a difference! This is true of Innovate for Vegas Initiatives and other Entities, and likely many other projects elsewhere.

## Overview Issues versus Component Project Issues

Initiative planning issues are found in the Overview Repository, which contains the Overview Component Project, the place to begin Bluesky ideation (the purpose and general notions driving an initiative as it begins and throughout its lifecycle). The Agile for Volunteers planning hierarchy (Theme, Epic, Feature, Story) will be found in the Issue structure here, in addition to externally-found Bugs that may or may not have an associated Component Project attached. That is, if someone not familiar with the Initiative and Component Project structure identifies and reports a Bug, it will be filed in the Overview Repository, triaged, and a corresponding Defect is created in the proper Component Project(s) Repository or Repositories.

Each Component Project repository contains Task issues related to the general Feature and Story planning issues found in the Overview repository. Tasks and Defects are assigned to specific Component Projects to which Volunteer Time, Effort, and Expertise are applied, so that any particular Component Project can advance through the relevant workflow for all involved without coupling to other Component Projects.

It is a design feature of Agile for Volunteers, that Issues within and between Component Project repositories within an Initiative will be related and most likely linked using issue-linking features of GitHub, though there may be a need on occasion to actually move an issue from one Component Project repository to another.

- [GitHub Doc: Transferring Issues Between Repositories](https://docs.github.com/en/issues/tracking-your-work-with-issues/transferring-an-issue-to-another-repository)
- [GitHub Doc: Issue and PR Linking](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/autolinked-references-and-urls#issues-and-pull-requests)

## Project Managers and Issue Tracking

Given the Volunteer structure of the Innovate for Vegas Foundation, it is unlikely that there will be a formal Project Manager role as one finds in many workplaces. Here we use the term as a familiar title, where within our Agile for Volunteers structure we will have Persistent Teams focused on Initiative efforts, generally and per Component Project, on a Continuous Flow timeline, as opposed to Iteration Flow timelines of Atomic Teams.

One of the responsibilities of a Project Manager is to keep track of Issues and the people filing issues, and make sure they are in the correct place (filed against the correct Component Project and its repository), that they are useful (make sure there is enough information to enable work to be done based upon the issue), and that they are not aging (bugs never go away by themselves!). The responsibilities of this role may be shared by more than one person, and may be tackled by people working with more than one Component Project. Wearing many hats, one might say.

Note all issues will be created by the individual who needs to create the issue. Consider an external customer from the community using an Initiative feature, who finds a problem and reports to Innovate for Vegas Foundation using some method other than the creation of a new Bug Issue. Capturing this issue is important, because mentions and chats and anecdotes are not a part of the project progress workflow itself, though they are the beginnings of identifying the actual defect or defects that require attention. These findings need to be converted into actual issues so that they can be further triaged and addressed. The source of the finding (with appropriate privacy awareness) should be noted in the issue for attribution, since taking the time to report Bugs is as valuable a contribution to our efforts as anything else.

## GitHub Projects

We are making use of the new style GitHub Project to keep track of Entities, including Initiative and Component Project repositories and their Issues.

As of this writing, this is a good place to begin learning about how GitHub has implemented the Issue tracking and Project management features that we will make use of for our Innovate for Vegas Foundation projects!

[GitHub Doc: Issues (and Projects)](https://docs.github.com/en/issues)
