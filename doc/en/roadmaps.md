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

# Initiative Roadmaps

Innovate for Vegas Foundation is made up of an all-volunteer contributor workforce; it is essentially impossible to commit people to tasks and tasks to a schedule given this structure. However, a general plan with an Initiative roadmap is possible so that those contributing their Volunteer Time, Effort, and Expertise have some idea what to expect regarding goals and direction, and can have some general awareness regarding progress of the team along the initiative path.

Each Initiative begins with an Initiative (prefix init-) Repository with top-level summary and repository links to provide an external visitor or passer-by an executive summary and map of components. An entrypoint if you will. The init- repository is always public to enable this use case, for anyone interested whether the Overview (prefix ov-) repository is available, public, or private. The Overview Repository begins as an empty repository, and soon contains the Draft Purpose or Bluesky documentation and then an ongoing collection of Initiative Planning Issues among other pieces of information.

Innovate for Vegas Foundation is not a commercial entity releasing products and services on a particular release schedule, recall we are an all-volunteer organization pursuing community elevation initiatives. As such, roadmaps are intended to provide information for volunteer contributors and casual observers, and are not intended in the general case to indicate a committed release schedule or feature set. Our Agile for Volunteers approach to Planning, Implementation, and Defect tracking will make the roadmap and progress along it, including changes, visible to all.

## Lifecycle

A new Initiative begins with something of a blank slate, there may only be some rough ideas, some blue sky notions, and some reference data and links. These are the ingredients of a Draft Purpose Document or what we also refer to as the Bluesky documentation (which belongs in the Overview, ov- , repository), and maybe include a vague and very rough roadmap, links to external resources and relevant projects and standards, and so on.

Note that in the Agile scheme, both with original Agile and our Agile for Volunteers implementation, User Stories and active, collaborative development will advance the Initiative and its Component Projects and will surface parts of the Overview that were not considered initially, or that make more sense with iterative ideation (and innovation) and implementation. The Overview phase and the ov- repository for a given Initiative should be considered works in progress throughout!

The Overview repository is created first among the Component Projects, and there may be any number of additional Component Project repositories associated with the Initiative over time. The Overview is the repository in which to create and maintain the Planning Backlog, including Theme, Epic, Feature, and Story issues. There is some detail in the [issues](issues.md) document concerning writing issues against the ov- repository and then referencing the issue in the relevant repository or repositories at some later time when these additional parts exist, within Task issues for implementation.

An example lifecycle start for an Example Initiative:

- Create the init-example repository
- Create the ov-example repository
- Create Bluesky Draft Proposal Documents describing at high level what the Initiative is about, what it will accomplish, we we are pursuing it, useful links and references, and so on
- We can begin a backlog of initial planning issues in the Overview repository
- Following the Whole-Team approach, continue to tune the Bluesky as needed, and add and edit Planning issues
- Create a Component Project repository and begin creating Task issues corresponding to Planning issues in the Overview
- Implement, and on from there…

As progress on an Initiative proceeds, Component Projects will be added, perhaps removed, merged, split, and so on, with the Overview capturing ongoing Planning, externally-identified Bugs, discussions and other interactions between external users or customers and the Whole Team working on the Initiative and Component Projects.

### Multiple Repositories

Component Projects are stored and tracked in repositories. In some cases there will be external elements (mechanical or other elements with a physical manifestation may have design files or other information in a repository but the physicality is not wholly stored and tracked there, for example), but all Initiative Component Projects should be visible via repository associations, starting with the Overview Repository and continuing through all of the additional, and potentially growing number of, Component Project Repositories.

As Initiative Planning continues, with Issues stored in the Overview Repository, one or more Component Project Repositories will be added or associated with the Initiative, with Implementation Task issues created in these repositories to describe and define the makeup of the Component and the work needed to implement the Planning Issues in the Overview. Use of issues in this workflow is described in the [Issues](issues.md) Howto document.

GitHub does support linking to issues across repositories, which is used for example to connect Planning Issues in the Overview Repository to Task Issues in a Component Project repository. A particular Planning Issue, eg a Story, might be implemented in one or more Component Projects, and so each will contain a Task describing the intended implementation details, linked back to the Story in the Overview Repository. This one-to-many relationship makes the connection between Component Projects within an Initiative observable.

[GitHub Doc: Issue and PR Linking](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/autolinked-references-and-urls#issues-and-pull-requests)

## Initiative Lifecycle

The Initiative roadmap will evolve through its life, which is the presumption with Agile workflows; we want to be responsive to the evolution of our Initiatives based on collaborative effort and feedback from our customers (see the [Agile](agile.md) document), including our end users and consumers, as well as other cohorts and even our own teams who may be using and re-using all or part of any particular Initiative. The Initiative itself may improve and evolve with bug fixes and feature additions, or it may split or merge to continue focused development in different directions.

### Component Lifecycles

As stated throughout, an Initiative includes or is made up of multiple components or Component Projects, each with a GitHub repository or equivalent (ideally a GitHub repository that can track external progress and be included in a GitHub project workflow would be a Good Thing), then at any given time a particular component will have some number of open issues to address, whether they are Bugs and Defects found in the field or in testing, or tasks to implement new Features or Stories. The Component lifecycle is a part of the Initiative lifecycle, in that the component will travel along its path as part of the Initiative doing the same, though possibly, even likely at different rates.

## Tools and Methods

Managing Initiatives and Component Projects and roadmaps and all of the various parts and the people building and maintaining those parts, is a full-time job for one or more people, depending on the size of a project. For volunteer organizations, the tasks are no less important, to manage each Initiative and its many parts, but volunteer time, effort, and expertise are not available as compensated worker time is for commercial endeavors. There will likely be a need for volunteers working on Innovate for Vegas Foundation Initiatives and Component Projects to contribute some time to the various management or general oversight responsibilities.

As will come up frequently, use of GitHub is not completely ideal in all situations, but there are some minimally useful project management tools that are a decent start. Any Innovate for Vegas Foundation Initiative and its Component Projects will have associated GitHub Projects, as can be seen by visiting here:

[GitHub Projects: Innovate for Vegas Foundation](https://github.com/orgs/InnovateForVegas/projects)

The view of issues across Component Project repositories for a given Initiative can be very useful, as can the Kanban view for one way of looking at movement along the roadmap for some parts of the Initiative and Component lifecycles. There are other tools, such as Gantt and PERT charts, that can be more useful for time and progress, especially if there are budget or delivery deadline concerns (not applicable for our volunteer-driven efforts, though we can learn from this possibility for scenarios in the future, or for participating in commercial or paid efforts elsewhere, thus a job skill).
