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

# Entity Naming

“There are only two hard things in Computer Science: cache invalidation and naming things.”—Phil Karlton

This is arguably applicable to nearly everything, from naming a child to naming a product to naming a company to naming a new star in a galaxy far, far away. Naming things can have contextual implications, cultural and linguistic implications, and regular old legal implications. They can also inform, or confuse, depending on which name you choose related to other names adjacent, in the present or in the future.

As with most things, there are various opinions when it comes to naming conventions, not to mention how best to express which version of that thing is available or in use or coming soon. For the sake of clarity, and to remove another few potential choices to make, we have some lines drawn in the sand regarding these two critically useful notions.

## Naming Repositories

There is a brief summary of this information in the CONTRIBUTING.md document for all Entities on which our Foundation is working, herein is an expanded treatise on the topic.

Each Entity will be comprised of many parts, some contained within repositories, others elsewhere but tracked by repositories. A top-level Initiative repo with this consistent naming scheme will help others to locate this top level and navigate the Initiative Component Project hierarchy, which will always include an OverView Component Project repo.

### Initiative Repo init-(name)

The top-most top-level repository, the Initiative encapsulates the notion, a public summary which will always be visible (the init- repositories are generally *no* marked private though there will likely be special cases where an init- repo is private) and is named to be easily identified.

This repository is likely to be slow to change once it is established, though it will be useful for top-level GitHub Team assignments and Component Project repository linking for various uses cases, not the least of which is determining which repositories are a part of a particular initiative (note: any Component Project repository may be a part of zero or more Initiatives).

### Overview Repo ov-(initiative-name)

This is the top-level OverView repository, which will contain a high-level description of the Initiative itself, a pro if available, and any other relevant high-level resources and information. As an aside, it is important to note that this part of any project may be the starting point against which a backlog of issues may be opened before actual project work in other repositories or other external workspaces begins to take place. By using this repository in this way, a convenient entry point with a well-known naming scheme will enable newcomers to a project to start at the beginning.

### General prefix scheme

Additional repositories added to the project should adhere to a similar naming scheme with several in use already and more may be added as needed. This convention will, ideally, make navigating the GitHub repository organizational scheme easier as more repositories are added. Note that adding a suffix to **project-name** is acceptable to indicate more detail (eg if there is more than one backend or frontend repo for a given project, perhaps using different technologies or methodologies, or other possibilities).

Here is a tabular example summary of some naming convention ideas that could make navigating a sea of repositories easier:

| Example Repository Name  | Description                                                                         |
|--------------------------|-------------------------------------------------------------------------------------|
| init-name                | A top-level, named Initiative to which Component Projects are attached              |
| ov-initiative-name       | Overview repository, top-level summary README, specs, dev documentation, etc        |
| be-component-py          | A backend part of the project, written mostly in python                             |
| fe-component-js          | A frontend part of the project, written in javascript                               |
| api-project-name         | A stand-alone API coded spec (OpenAPI, etc) platform independent                    |
| spi-project-name         | A System Programming Interface, an API for internal use (between services, etc)     |
| db-project-sql           | A database schema definition in sql                                                 |
| doc-project              | Project documentation intended for external use (users, developers, etc)            |
| app-project-js           | A stand-alone or native application component of a project                          |
| ui-project               | User Interface designs and elements, possibly in html, svg, etc                     |

Organization of each repository, and of project components not stored within GitHub or a git repository in general, are likely to have their own particular needs based on programming language, architectural choices, and sensibility. Aside from inclusion of LICENSE and other standard files to comply with the Innovate for Vegas open source development and publishing scheme, naming conventions and repository organization are left to the contributors and consensus per repository.

### Reasoning behind name prefixes

GitHub does not make it easy to group projects. The repository tags (see next section) are useful, but not sufficient, and it is possible to use the star feature and group stars by named list. These are not ideal, where a way of grouping by directory might be more so.

The choices for structured repository naming come down to either a fixed Entity name prefix, a language or framework prefix, or a repository type prefix. The name of the repository may vary from the Entity name per Entity repository as appropriate (for example, within the Smart Social Initiative, there is a repository called be-smart-calendar-server-py which does not explicitly include the Initiative name but which is a Component Project of same), and it we can group Entities with the repository tags detailed below, where the tags themselves have the problem use cases described.

For structured naming, then, and with GitHub presenting repositories sorted most easily by name or last-commit date (that is, Last Update, Name, and the not-useful Stars sort options) in the browser based interface, a prefix that indicates the repository type (see table above for examples) will naturally sort repositories into type sections, with the name of the project component useful thereafter to drill down to the desired component(s). Additional information in a suffix allows for similarly-named project components implemented in multiple ways, or with multiple types of external tools, and so on.

Note also, this naming scheme is useful outside of GitHub, if there are multiple repositories in your local environment you can quickly sort and identify which is for what. In a local development directory structure it is also possible, perhaps recommended, to use folders or directories to group Initiative repositories together.

### Entity Repository Naming Example

| Example Repository Name       | Description                                                                         |
|-------------------------------|-------------------------------------------------------------------------------------|
| init-open-transit             | Top of the Initiative collection                                                    |
| ov-open-transit               | Top-level overview repository                                                       |
| fe-open-transit-consumer-quik | A front-end Open Transit client using the Quik (js) framework                       |
| db-open-transit-consumer-sql  | An SQL database schema design for Open Transit Consumer Data stores                 |
| api-open-transit-consumer     | A language-agnostic API spec (eg OpenAPI) for Consumer features                     |
| be-open-transit-consumer-py   | A back-end Open Transit server for consumer application interfacing                 |

The number of Component Projects may change over time, and there is room for experimentation and retiring of one or more repositories in favor of one or more others, and so on. A search by project name will be useful, but since in this example each repository contains the project name (ie open-transit) the search results will be conclusive, if at any time a repository is added called eg bus-rider it would be effectively hidden from search results without prior knowledge. This naming scheme does not address that at all, other than increase the possibility of coming across this naming variation if one is looking for front-end projects and fe-bus-rider appears in the result set.

### Naming other things

Many frameworks and some languages have a preferred or de facto naming scheme, especially when a skeletal project or scaffolding tool is used to start a project. In these cases, it is useful to follow the naming scheme for that platform or framework or language, since familiarity will help others when they join the project, or if you yourself move from one project to another. Naming files and components using common and well-known patterns can save time and help to ascend the learning curve.

Naming of variables and functions and other modules is the topic countless articles, books, lectures, YouTube and other tutorial videos, and repository discussions. If we revisit the quote by Phil Karlton one last time, it certainly applies here, to a place in your workflow where expedience or convenience or fatigue or various other factors lead to CamelCase, hyphenated-variables, type prefix tpLetters, under_scores, uselessly-named index or counter variables (i, x, n), confusing function names that doit(): but what exactly, and the list of possibilities continues. If there is a pattern set in the project repository, try to continue that, but make note of whether the selected naming scheme is useful, confusing, or otherwise. It is one of the two hard problems, after all.

If there is a Style Guide within a particular Component Project Repository, and/or if the Initiative sets forth a style guide to apply to all Component Projects, these should be followed by all contributors to these Entities.

### Repository Topic Tags

GitHub enables use of repository tags to help locate repositories. These are global to the GitHub platform and will reveal all public repositories to all seeking a matching tag, which can be useful in some cases for broad discovery but less than useful in others such as grouping our organization repositories in useful ways. They are visible in a Topic search on GitHub.

The smallest useful administrative unit of for our purposes within git and GitHub (and GitLab and others) is the project repository, and in an organization with many contributors the number of individual repositories associated with one or more projects can grow quickly. The ability to sort and group and search and list repositories can become a bit of a challenge. The tagging scheme can be useful, even with the caveat that tags on public repositories are visible globally. We can make an effort to isolate our own tags for our own sorting needs withing our organization.

We can accomplish some isolation by prefixing our repository tags with a known and uncommon prefix and hyphen, not unlike the repository naming scheme described above. Thus

A tag *opentransit* may show up across countless projects within GitHub (though as of this writing, it is unused globally, though there are opentransit project names to be found in a GitHub search). Using the naming prefix will avoid losing our limited search result set to a larger adoption of a particular topic tag later.

This is not a guarantee, but it does make organization-wide topic tags more useful for a longer period of time. It is also possible and simple to add additional topic tags so that particular repositories **do** appear in searches for related topics. For example, a *python* or *postgresql* topic tag will place a particular project into those topics, along with eg *ifv-opentransit*.

You can visit the top level Topics section of GitHub for more information and to search and browse topics:

[GitHub Topics](https://github.com/topics)

## References

[Naming Things Book](https://www.namingthings.co/)
