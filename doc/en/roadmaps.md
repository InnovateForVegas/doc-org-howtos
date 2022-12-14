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

# Project Roadmaps

Projects commence frequently. As of this writing, a new project topic is initiated each month, aligned with an overarching capstone project to connect everything in a grand scheme. Each project is a stand-alone undertaking as well. That is, each individual project or project topic, could stand on its own (though have designed to function in concert).

Since Innovate for Vegas Foundation is an all-volunteer work force, it is difficult to commit people to tasks and tasks to a schedule. However, a general plan with a project roadmap is possible.

Each project topic begins with an Overview captured in an ov- repository. This is where a roadmap belongs, initially through implication, and in some short interval, a rough idea of what needs to be done and in which order so that the various sub-components can align and result in some useful, or at least testable functionality. If we only finish a piece of the roadmap, those completed or nearly-completed pieces may or may not be so useful without the other half of that part of the roadmap, then what?

Note: Since initially composing this Howto, we have begun an experiment to adopt a [Volunteer Agile](agile.md) workflow. Since Agile was not really designed for Volunteers, it will be an interesting experiment!

## Overview Lifecycle

On init of a project overview repository, there may only be some rough ideas, some blue sky notions, and some reference data and links. These are the ingredients of a more formal project description (which still belongs in the Overview, ov- , repository), roadmap, and other high-level documentation.

Note that in the Agile scheme, this early stage of project specification does not receive so much focus. User Stories and active, collaborative development will advance the project and will surface parts of the overview that were not considered initially, or that make more sense with iterative ideation and implementation. The Overview phase and the ov- repository for a given project should be considered works in progress throughout!

Since the overview repository is created first, and there may be any number of component and sub-component repositories associated with the project over time, the Overview project is a great repository against which to create and maintain the initial Backlog, which is basically a to-do list before actual work on the project itself has commenced. There is some detail in the [issues](issues.md) document concerning writing issues against the ov- repository and then referencing the issue in the relevant repository or repositories at some later time when these additional parts exist.

Using the Open Transit project as an example:

* We create the ov-open-transit project
* We create and update various idea, spec, and reference documents for the project
* We can spell out a very rough roadmap and timeline if we have targets and deliverables in mind, this is not always the case
* We can create a backlog of initial work, as User Stories, such as:
  * We need a user interface for transit users (eg bus riders)
  * We need a data back end to capture and analyze real-time bus location info
  * Etc
* Create a front end (fe-) repository and begin work on front end user interfaces
* And so on...

Once we are creating additional components (and these may be code repositories in GitHub directly, or some or all of the project work may be completely outside of GitHub, in which case a progress tracking repository or files within a given repository will be extremely useful to fit into the overall project management workflow) we can move the Backlog issues from the Overview repository to the relevant component repository (so the fe- repository in the example above) and update any roadmap and architecture plans in the overview accordingly.

## Multiple Repositories

If we stick with our Open Transit example, suppose one team is going to implement a solution to one of the ov- Backlog items using a React-based architecture, while another team is aiming at an Angular-based solutions. We will have **two** repositories in the fe- category for this part of the Open Transit project.

Backlog issues in the Overview repository will probably not have to much history before they are actually a part of some project repo, but there may actually be some commentary or other information attached. This is why it is important to make repository-specific copies of issues that refer to the top level User Story. This is described someone in the [Issues](issues.md) Howto.

### Copy the Overview Issue to Each Repository And Link

In this case, we can assume that two or more repositories that are working on the same issue(s) in different ways to accomplish similar outcomes are beginning close in time. It makes sense to copy the original issue in the backlog to each new repo as part of their respective beginnings.

As is always the case, this is a fork of the original issue and they will diverge in each project. This is completely acceptable in this case, since each project will make decisions and change directions as the team sees fit to accomplish the goal, but it is something to be aware of. Since the two issues have a common origin, it is possible that the divergence will yield some new information in each part of the fork, so it would be worthwhile to compare notes, so to speak, on the differences over time. This is a great item for a project manager to pay attention to.

GitHub does support linking to issues in other repositories. It is a small amount of extra effort, but it is possible to link an issue in a particular component repository backlog to an issue in the overview backlog (and link back, for a double link) so  that there is a specific relationship that can be visited as needed through the development process.

[GitHub Doc: Issue and PR Linking](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/autolinked-references-and-urls#issues-and-pull-requests)

In the React versus Angular example, the Backlog User Story in the Overview is the source, a copy of the User Story Issue in each of the React and Angular repositories links back to the Overview Backlog User Story, and each of the two project repositories captures development effort addressing the respective version of the User Story at different rates, with different discussions and perhaps different outcomes. The original User Story is preserved (and may be discussed and modified over time) while each project repository has the same process of discussion, implementation, and progress tracking.

### Maintain a Single Issue

This is almost not worth mentioning, since it would take some creativity beyond the scope of this document. However, let us imagine a potential method here.

Unless some method can be devised making use of GitHub/Git methodologies (or external tools that can integrate in useful ways), to track progress in multiple divergent repositories in one single top-level Backlog Issue (in the ov- Backlog or elsewhere), it is probably not worthwhile compared with the Copy-and-Link scheme previously described.

The only cases that make sense for single-issue tracking likely involve administrative or other top-level-project Issues, rather than implementation Issues.

## Project Lifecycle

The project roadmap will evolve through its life, which is the presumption with Agile workflows; we want to be responsive to the evolution of our projects based on collaborative effort and feedback from our customers (see the [Agile](agile.md) document), with bug fixes and feature additions and other evolutions. A major change, such as a substantial departure in feature set or a change to a completely new framework or style or language may lead to a temporary fork in the roadmap (that is, some effort will go down the new path while some effort will go toward maintaining the main path), but the fork would merge back into a main development path when the fork and its new features and whatnot are ready to be released to the world. This is similar to the Feature Branch approach you may know about, but project-scoped.

### Component Lifecycles

If we assume, as we have throughout, that a project such as Open Transit will include multiple components, each with a GitHub repository or equivalent (ideally a GitHub repository that can track external progress and be included in a GitHub project workflow would be a Good Thing), then at any given time a particular component will have some number of open issues to address, whether they are problems found in the field or in testing, or features to add, or enhancements to consider, etc. The component lifecycle is a part of the project lifecycle, in that the component will travel along its path as part of the project doing the same.

This is something of a hand wave, but since each project will be different in its makeup and focus, and each will have varying types and numbers of components, it is impossible to make blanket statement about specific lifecycle considerations. Generally speaking, though, issues which are problems to *fix* will not impact the project lifecycle (these are fixes to existing features and functionalities) while feature additions and changes, and anything that would be considered a major version change, will possibly impact the project lifecycle.

By way of example, again with the Open Transit project:

If the  Open Transit project is in a released state with all components stable and functional with occasional issues found and addressed as fixes, it is possible that a major change in the way the public transportation system functions, or perhaps there will be a new form of transportation rolled into the system (a monorail, a subway, perhaps flying cars, etc). In this case, one or more components may need new features and enhancements, which will have an impact in how the project as a whole functions.

If a change to any particular project component has an impact on another project component, the project lifecycle is impacted. If the Open Transit backend data server requires major changes to support new transportation modes, the frontend may require new user interface elements and new api accesses, and most likely some new user interface design considerations, new and changed graphical elements, new accessibility considerations, and there may even be a need for entirely new components.

## Project Forks

There may also be the possibility that a particular project will require an entire fork in a new direction but as a relative of the original. Sticking with Open Transit, suppose there is a fundamental change to the requirements of a particular transit system that are so drastically different compared with the RTC configuration used in Southern Nevada, that the new project itself is simply not compatible with the main project. In this case, the creation of a related transit fork would be reasonable, though this would be worth serious consideration if the project fork is actually essential. It would be difficult to imagine a project fork (that is, a completely new lifecycle and development timeline and path and everything that takes development of the new relative away from the original project) that could not be accomplished with a project-scoped feature fork as described above, unless the new project becomes its own effort. If the project is forked, it is possible that some of the original components will also require forks, and some may be compatible across projects.

This can quickly become complicated, but it is something to think about in passing (do not spend much more than a few moments on the possibility, a project fork is unlikely). If we were to take an actual example of a project fork from the real world, we can look at the something like the Netscape browser project at the time it was going to be converted into the Mozilla project (Note that Netscape also had a server project, and this is a dramatic simplification of all of the various bits of work into these two project ideas). There was a project fork of the Netscape web browser into the initial Mozilla browser, at which point all of the parts that were not compatible with the open source license of the Mozilla project were replaced or removed and any documentation and build system and graphical elements and user interface designs and so on were updated, such that some components were forked and modified, others were used without modification, and some were created as part of the new project fork. Eventually, AOL purchased Netscape and the browser project, leaving Mozilla and the Firefox browser to continue on.

## Tools and Methods

Managing projects and roadmaps and all of the various parts and the people building and maintaining those parts, is a full-time job for one or more people, depending on the size of a project. For volunteer projects, the task is no less important, to manage a project and its moving parts, but it can be difficult to rely completely on a single point of failure (ie the project manager(s) may not have the time for whatever reason, they may depart the project temporarily or permanently, etc) so there will likely be a need for volunteers working on Innovate for Vegas Foundation projects to contribute some time to the various project management responsibilities.

As will come up frequently, use of GitHub is not completely ideal in all situations, but there are some minimally useful project management tools that are a decent start. Any Innovate for Vegas Foundation project will have an associated GitHub Project feature, as can be seen by visiting here:

[GitHub Projects: Innovate for Vegas Foundation](https://github.com/orgs/InnovateForVegas/projects)

The view of issues across component repositories for a given project can be useful, as can the Kanban view for one way of looking at movement along the project roadmap for some parts of the project and component lifecycles. There are other tools, such as Gantt and PERT charts, that can be more useful for time and progress, especially if there are budget or delivery deadline concerns. While projects may not have these considerations initially or as part of the Innovate for Vegas Foundation efforts, they may graduate to revenue-generating deployment or external development relationships with municipal partners, at which point these additional project management tools and methods will be useful. It will be a valuable addition to the job skills toolbox (for all, not only software coders) to learn how projects and the tools to manage them actually work, especially with the people who are making the project go as a part of the process.
