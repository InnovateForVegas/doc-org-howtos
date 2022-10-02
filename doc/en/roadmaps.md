<!--
 Copyright (C) 2022 Code for Vegas Foundation
 
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

Since Code for Vegas Founation is an all-volunteer work force, it is difficult to commit people to tasks and tasks to a schedule. However, a general plan with a project roadmap is possible.

Each project topic begins with an Overview cepatured in an ov- repository. This is where a roadmap belongs, initially through implication, and in some short interval, a rough idea of what needs to be done and in which order so that the various sub-components can align and result in some useful, or at least testable functionality. If we only finish a piece of the roadmap, those completed or nearly-completed pieces may or may not be so useful without the other half of that part of the roadmap, then what?

## Overview Lifecycle

On init of a project overview repository, there may only be some rough ideas, some blue sky notions, and some reference data and links. These are the ingredients of a more formal project description (which still belongs in the Overview, ov- , repository), roadmap, and other high-level documentation.

Since the overview repository is created first, and there may be any number of component and sub-component repositories associated with the project over time, the Overview project is a great repository against which to create and maintain the initial Backlog, which is basically a to-do list before actual work on the project itself has commenced. There is some detail in the [issues](issues.md) document concerning writing issues against the ov- repository and then moving the issue to the relevant repository at some later time when the repository exists.

Using the Open Transit project as an example:

* We create the ov-open-transit project
* We can create a backlog of initial work
  * First, we need more info and a roadmap!
  * We need a user interface for transit users (eg bus riders)
  * We need a data back end to capture and analyze real-time bus location info
  * Etc
* Create a front end (fe-) repository and begin work on front end user interfaces
* And so on...

Once we are creating additional components (and these may be code respositories in GitHub directly, or some or all of the project work may be completely outside of GitHub, in which case a progress tracking repository or files within a given repository will be extremely useful to fit into the overall project management workflow) we can move the Backlog issues from the Overview repository to the relevant component repository (so the fe- repository in the example above) and update any roadmap and architecture plans in the overview accordingly.

## Multiple Repositories

If we stick with our Open Transit example, suppose one team is going to implement a solution to one of the ov- Backlog items using a React-based architecture, while another team is aiming at an Angular-based solutions. We will have **two** repositories in the fe- category for this part of the Open Transit project.

Backlog issues in the Overview repository will probably not have to much history before they are actually a part of some project repo, but there may actually be some commentary or other information attached. There are two ways to approach this:

### Copy the Overview Issue to Each Repository

In this case, we can assume that two or more repositories that are working on the same issue(s) in different ways to accomplish similar outcomes are beginning close in time. It makes sense to copy the original issue in the backlog to each new repo as part of their respective beginnings.

As is always the case, this is a fork of the original issue and they will diverge in each project. This is completely acceptable in this case, since each project will make decisions and change directions as the team sees fit to accomplish the goal, but it is something to be aware of. Since the two issues have a common origin, it is possible that the divergence will yield some new information in each part of the fork, so it would be worthwhile to compare notes, so to speak, on the differences over time. This is a great item for a project manager to pay attention to.

### Maintain a Single Issue

This is almost not worth mentioning, since it would take some creativity beyond the scope of this document. However, let us imagine a potential method here.

Suppose we have a repository that can track both the React and the Angular versions of the front end component. In that case, the issue would be updated with findings based on progress in each repository. This is essentially a continuous comparison as would occur with an issue fork, where the issue is always tracking all forks.

There are not great options to accomplish this with Git or GitHub. Branches, one for each of React and Angular in our example, would become cumbersome if they were easily usable, but GitHub actually flips that notion around and associates a branch with an issue as a way to manage work on an issue and the eventual merge process.

The hybrid manual+GitHub approach might be to keep the issue in the ov- backlog and create copies of the issue as with the fork example, and then contiuously update the ov- backlog issue from each of the forked issues. This becomes tedious and error-prone as projects grow, so also not recommended.

Similarly, one fe- repository may be forked from another.

This is probably not too easy to achieve, so issue forks seem likely, IF there are multiple variants of a particular component.
