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

# Project Roadmaps

Projects commence frequently. As of this writing, a new project topic is initiated each month, aligned with an overarching capstone project to connect everything in a grand scheme. Each project is a stand-alone undertaking as well. That is, each individual project or project topic, could stand on its own (though have designed to function in concert).

Since Innovate for Vegas Foundation is an all-volunteer work force, it is difficult to commit people to tasks and tasks to a schedule. However, a general plan with a project roadmap is possible.

Each project topic begins with an Overview captured in an ov- repository. This is where a roadmap belongs, initially through implication, and in some short interval, a rough idea of what needs to be done and in which order so that the various sub-components can align and result in some useful, or at least testable functionality. If we only finish a piece of the roadmap, those completed or nearly-completed pieces may or may not be so useful without the other half of that part of the roadmap, then what?

## Overview Lifecycle

On init of a project overview repository, there may only be some rough ideas, some blue sky notions, and some reference data and links. These are the ingredients of a more formal project description (which still belongs in the Overview, ov- , repository), roadmap, and other high-level documentation.

Since the overview repository is created first, and there may be any number of component and sub-component repositories associated with the project over time, the Overview project is a great repository against which to create and maintain the initial Backlog, which is basically a to-do list before actual work on the project itself has commenced. There is some detail in the [issues](issues.md) document concerning writing issues against the ov- repository and then moving the issue to the relevant repository at some later time when the repository exists.

Using the Open Transit project as an example:

* We create the ov-open-transit project
* We create and update various idea, spec, and reference documents for the project
* We can create a backlog of initial work, such as:
  * First, we need more info and a roadmap!
  * We need a user interface for transit users (eg bus riders)
  * We need a data back end to capture and analyze real-time bus location info
  * Etc
* Create a front end (fe-) repository and begin work on front end user interfaces
* And so on...

Once we are creating additional components (and these may be code repositories in GitHub directly, or some or all of the project work may be completely outside of GitHub, in which case a progress tracking repository or files within a given repository will be extremely useful to fit into the overall project management workflow) we can move the Backlog issues from the Overview repository to the relevant component repository (so the fe- repository in the example above) and update any roadmap and architecture plans in the overview accordingly.

## Multiple Repositories

If we stick with our Open Transit example, suppose one team is going to implement a solution to one of the ov- Backlog items using a React-based architecture, while another team is aiming at an Angular-based solutions. We will have **two** repositories in the fe- category for this part of the Open Transit project.

Backlog issues in the Overview repository will probably not have to much history before they are actually a part of some project repo, but there may actually be some commentary or other information attached. There are two ways to approach this:

### Copy the Overview Issue to Each Repository And Link

In this case, we can assume that two or more repositories that are working on the same issue(s) in different ways to accomplish similar outcomes are beginning close in time. It makes sense to copy the original issue in the backlog to each new repo as part of their respective beginnings.

As is always the case, this is a fork of the original issue and they will diverge in each project. This is completely acceptable in this case, since each project will make decisions and change directions as the team sees fit to accomplish the goal, but it is something to be aware of. Since the two issues have a common origin, it is possible that the divergence will yield some new information in each part of the fork, so it would be worthwhile to compare notes, so to speak, on the differences over time. This is a great item for a project manager to pay attention to.

GitHub does support linking to issues in other repositories. It is a small amount of extra effort, but it is possible to link an issue in a particular component repository backlog to an issue in the overview backlog (and link back, for a double link) so  that there is a specific relationship that can be visited as needed through the development process.

[GitHub Doc: Issue and PR Linking](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/autolinked-references-and-urls#issues-and-pull-requests)

### Maintain a Single Issue

This is almost not worth mentioning, since it would take some creativity beyond the scope of this document. However, let us imagine a potential method here.

Suppose we have a repository that can track both the React and the Angular versions of the front end component. In that case, the issue would be updated with findings based on progress in each repository. This is essentially a continuous comparison as would occur with an issue fork, where the issue is always tracking all forks.

There are not great options to accomplish this with Git or GitHub. Branches, one for each of React and Angular in our example, would become cumbersome if they were easily usable, but GitHub actually flips that notion around and associates a branch with an issue as a way to manage work on an issue and the eventual merge process.

The hybrid manual+GitHub approach might be to keep the issue in the ov- backlog and create copies of the issue as with the fork example, and then continuously update the ov- backlog issue from each of the forked issues. This becomes tedious and error-prone as projects grow, so also not recommended.

Similarly, one fe- repository may be forked from another.

This is probably not too easy to achieve, so issue forks seem likely, **if** there are multiple variants of a particular component.

Unless some method can be devised making use of GitHub/Git methodologies, to track progress in multiple divergent repositories in one single top-level issue (in the ov- Backlog or elsewhere) is probably not worthwhile compared with the Copy-and-Link scheme previously described, unless projects grow to exceptional size. In these cases, it would be more appropriate to investigate external issue tracking tools (eg Jira).

## Project Lifecycle

The project roadmap will likely adjust slightly during the early part of its timeline, but eventually the main development line of a top-level project will most likely become a fairly stable and straight line, with bug fixes and feature additions and other evolutions. A major change, such as a substantial departure in feature set or a change to a completely new framework or style or language may lead to a temporary fork in the roadmap (that is, some effort will go down the new path while some effort will go toward maintaining the main path), but the fork would most likely merge back into a main development path when the fork and its new features and whatnot are ready to be released to the world.

### Component Lifecycles

If we assume, as we have throughout, that a project such as Open Transit will include multiple components, each with a GitHub repository or equivalent (ideally a GitHub repository that can track external progress and be included in a GitHub project workflow would be a Good Thing), then at any given time a particular component will have some number of open issues to address, whether they are problems found in the field or in testing, or features to add, or enhancements to consider, etc. The component lifecycle is a part of the project lifecycle, in that the component will travel along its path as part of the project doing the same.

This is something of a hand wave, but since each project will be different in its makeup and focus, and each will have varying types and numbers of components, it is impossible to make blanket statement about specific lifecycle considerations. Generally speaking, though, issues which are problems to *fix* will not impact the project lifecycle (these are fixes to existing features and functionalities) while feature additions and changes, and anything that would be considered a major version change, will possibly impact the project lifecycle.

By way of example, again with the Open Transit project:

If the  Open Transit project is in a released state with all components stable and functional with occasional issues found and addressed as fixes, it is possible that a major change in the way the public transportation system functions, or perhaps there will be a new form of transportation rolled into the system (a monorail, a subway, perhaps flying cars, etc). In this case, one or more components may need new features and enhancements, which will have an impact in how the project as a whole functions.

If a change to any particular project component has an impact on another project component, the project lifecycle is impacted. If the Open Transit backend data server requires major changes to support new transportation modes, the frontend may require new user interface elements and new api accesses, and most likely some new user interface design considerations, new and changed graphical elements, new accessibility considerations, and there may even be a need for entirely new components.

## Project Forks

There may also be the possibility that a particular project will require an entire fork in a new direction but as a relative of the original. Sticking with Open Transit, suppose there is a fundamental change to the requirements of a particular transit system that are so drastically different compared with the RTC configuration used in Southern Nevada, that the project itself is simply not compatible with the main project. In this case, the creation of a related transit fork would be reasonable, though this would be worth serious consideration if the project fork is actually essential. It would be difficult to image a project fork (that is, a completely new lifecycle and development timeline and path and everything that takes development of the new relative away from the original project). If the project is forked, it is possible that some of the original components will also require forks, and some may be compatible across projects.

This can quickly become complicated, but it is something to think about in passing (do not spend much more than a few moments on the possibility, a project fork is unlikely). If we were to take an actual example of a project fork from the real world, we can look at the Netscape browser project at the time it was going to be converted into the Mozilla project (Note that Netscape also had a server project, and this is a dramatic simplification of all of the various bits of work into these two project ideas). There was a project fork of the Netscape web browser into the initial Mozilla browser, at which point all of the parts that were not compatible with the open source license of the Mozilla project were replaced or removed and any documentation and build system and graphical elements and user interface designs and so on were updated, such that some components were forked and modified, others were used without modification, and some were created as part of the new project fork. Eventually, AOL purchased Netscape and the browser project, leaving Mozilla and the Firefox browser to continue on.

## Tools and Methods

Managing projects and roadmaps and all of the various parts and the people building and maintaining those parts, is a full-time job for one or more people, depending on the size of a project. For volunteer projects, the task is no less important, to manage a project and its moving parts, but it can be difficult to rely completely on a single point of failure (ie the project manager(s) may not have the time for whatever reason, they may depart the project temporarily or permanently, etc) so there will likely be a need for volunteers working on Innovate for Vegas Foundation projects to contribute some time to the various project management responsibilities.

As will come up frequently, use of GitHub is not completely ideal in all situations, but there are some minimally useful project management tools that are a decent start. Any Innovate for Vegas Foundation project will have an associated GitHub Project feature, as can be seen by visiting here:

[GitHub Projects: Innovate for Vegas Foundation](https://github.com/orgs/CodeForVegas/projects)

The view of issues across component repositories for a given project can be useful, as can the Kanban view for one way of looking at movement along the project roadmap for some parts of the project and component lifecycles. There are other tools, such as Gantt and PERT charts, that can be more useful for time and progress, especially if there are budget or delivery deadline concerns. While projects may not have these considerations initially or as part of the Innovate for Vegas Foundation efforts, they may graduate to revenue-generating deployment or external development relationships with municipal partners, at which point these additional project management tools and methods will be useful. It will be a valuable addition to the job skills toolbox (for all, not only software coders) to learn how projects and the tools to manage them actually work, especially with the people who are making the project go as a part of the process.
