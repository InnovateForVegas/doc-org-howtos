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

# GitHub and Innovate for Vegas Foundation

GitHub is a useful platform for a variety of things. Because it is essentially free to use for our needs.

We ask that those who would like to participate in projects, whether they are CodeFor or CreateFor or somewhere in between (or maybe even neither), because we will be using some of the project management features that GitHub offers, and we can make these tools a part of our attribution project so that when anyone applying for [jobs](jobs.md) or pursuing any avenues where a reference to contributed work is needed and beneficial, we can point right here!

## Getting Started

If you do not already have a GitHub account, please [sign up for one](https://github.com/). That part is completely free and it's a good idea to become familiar with this tool, and we are using it for important parts of our collaboration and project management workflows. If you already have a GitHub account but you want to keep your work with the [InnovateForVegas Organization](https://github.com/InnovateForVegas) separate, please do sign up for a new account and manage the use of that account for the participation you would like it associated with!

[GitHub Doc: Signing Up for a GitHub Account](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account)

Once you have an account, you will probably want to familiarize yourself with how to use it. GitHub has built up a reasonable set of documentation, starting here might be a good idea:

[GitHub Doc: Getting Started with your Account](https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account) .

If you have never used Git or GitHub before, there is a lot to learn, but starting out with reading this document and the other Howto information we are creating for our volunteers, looking at other repositories and reading other related documentation, watching various YouTube video tutorials, and simply asking questions of your fellow volunteers will help you become familiar.

[GitHub Doc: GitHub Cheatsheets](https://docs.github.com/en/get-started/quickstart/git-cheatsheet)

If you want to take a crash course in Git and GitHub, there is a very reasonable tutorial offered by freeCodeCamp here:

[YouTube: Git and GitHub For Beginners](https://www.youtube.com/watch?v=RGOj5yH7evk)

## Permissions

Personal GitHub accounts (you probably have one, you should!) allow for the creating of fine-grained access tokens and control of your private and public repositories, the idea being that you own your personal account and its contents.

The *InnovateForVegas* GitHub organization has owners, maintainers, teams, and multiple people associated with those roles, so things get slightly more complicated (but luckily not complex). Here are some links to look over if you have questions about access configuration, and of course if something seems to be configured incorrectly or non-ideally, say something!

[GitHub Doc: Roles in Organizations](https://docs.github.com/en/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization#about-organization-roles)
[GitHub Doc: Team Maintainers](https://docs.github.com/en/organizations/organizing-members-into-teams/assigning-the-team-maintainer-role-to-a-team-member)
[GitHub Doc: Repository Roles for an Organization](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/repository-roles-for-an-organization)

## Projects and Repositories

We are using the new form of GitHub Project to organize repository-based project issues, which are used to track progress through individual repository lifecycles. How does that sound?

Let us examine that more closely:

We are pursuing monthly projects that are all going to make up some part of the capstone project. Our first capstone is Virtual Vegas, and so projects addressing transit, open data, human interface, identity, and so on, all form parts of this overarching capstone.

Each project will consist of at least one, and likely many more components, which we can track and manage within the GitHub infrastructure (except in cases where we cannot…), and we can map our projects to GitHub projects, and the actual component parts of our projects to GitHub component repositories as part of GitHub projects.

There is a top-level view of all organization projects that have been created (and are open, in the default view here), you can visit that page for our organization and see a list of projects to begin examining them:

[InnovateForVegas Projects](https://github.com/orgs/InnovateForVegas/projects)

Since this is a live document, you will need to visit that link and discover the state of a given project at any given time, but suffice to say, as we gain traction using the [issue](issues.md) system per repository, we will begin to see how project management across project components can be an interesting challenge, made slightly easier with tools such as those GitHub offers (there are better, more capable, and much more expensive tools, to be sure).

## Repository Naming and Tagging

As more people contribute to more projects and more project repositories are created, it will become more and more difficult to locate what you are looking for within our GitHub organization. Until GitHub introduces a folder-like interface to group repositories, we need a workaround!

First of all, a prefix helps with sorting and grouping in English Alphabet alphabetical order. These also give some indication of what the repository is for.

For examples, Overview Repositories will begin with a leading *ov-* and will be named for the project itself, ie

[ov-open-transit](https://github.com/InnovateForVegas/ov-open-transit)

[ov-smart-social](https://github.com/InnovateForVegas/ov-smart-social)

As well, each of these is tagged with a cfv- and ifv- tag per project, which will make it easier to group InnovateForVegas org repos by project. Tag names begin with *cfv-* since GitHub does not allow namespaced tags, so that if one were to tag a repository with *javascript* then ALL repositories with that tag are returned in a search. Constrained searches are available, but we can easily begin by tagging InnovateForVegas project repositories with the *cfv-* and *ifv-* formatted tags and achieve some convenience directly.

**Note**: GitHub tags are for our convenience, git tags are a part of the revision control scheme and are a different thing. If you are curious about this, start at the reference link below…

## Signed Commits

Should you sign your commits? **Yes**.

Innovate for Vegas Foundation will be leaning heavily toward encryption, security, authentication, and all of these other readily-available technologies and methods and protocols that have existed for decades, but which many do not use! We aim to change this to make a more secure and privacy-aware Smart City!

What is a signed commit? Read here:

[GitHub Doc: Signing Your Commits](https://docs.github.com/en/authentication/managing-commit-signature-verification/signing-commits)

Use of GPG keys (GPG stands for Gnu Privacy Guard and is an homage to Phil Zimmerman’s PGP, or Pretty Good Privacy, which brought real public key cryptography to the masses decades ago!) is the easiest way to start, and when you generate your key pair (one set of instructions is in the signing documentation there, there are other ways and they all work) you will start the journey toward becoming familiar with how public key cryptography works. This is a great thing.

## Two Factor Authentication

Should you enable two factor authentication on your account? **Yes**.

In fact, you should enable two factor authentication (usually abbreviated 2FA and sometimes U2F for Universal 2 Factor) anywhere you can, if for no other reason than to reduce the chance you will have an account hijacked and your stuff taken from you from one errant click (there is a caveat to that, but it is not untrue). For GitHub use, though, we use it, you should also, here is the beginning of their documentation:

[GitHub Doc: About 2FA](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/about-two-factor-authentication)

Continue reading the next articles linked within that first one and see how it works. It is not difficult, we use a hardware token device (a Yubikey) and a TOTP value generator similar to the Google Authenticator that came out a decade or so ago. Depending entirely on a username and password is risky, do the right thing for yourself, our organization, and the future of humanity (really, seriously).

Caveat: If you are already logged into an account, whether it is your ancient and dead Facebook account, or your shiny GitHub account, the second factor is not always checked in all potentially-risky situations. If you are logged in to an account and you happen to click on a phishing email that takes advantage of that, you may run into trouble. However, most of the time the service in question will require you to verify your login credentials, ideally with your 2FA, to do critical things, for example changing your password or deleting your account. Learn to use 2FA and make it a great habit, and make sure you lobby for its use in products and service you work in into the future!

## GitHub Discussions and Issues

If you would like to participate in a project but you are not quite comfortable yet to edit code or start your own repository or all of the other fun stuff, consider reviewing a repository and adding to the Discussion for that repository, or consider creating a new Issue for that repository. These are relatively easy (especially a Discussion item, very similar to participating in any discussion forum anywhere) and will offer value to the project and team!

Filing an Issue may seem more complicated, but remember that an Issue is just a more formal Discussion item that is assigned to a person and which can be used to track a change to the project repository later. This sounds complicated, it is not. An Issue is a *To Do* item. Any Discussion can be converted to an Issue and vice versa. Each Project Repository has Discussions enabled (if you find a repository that does not, it should or will), and all repositories have Issues enabled.

These might be useful documents to read through:

[GitHub Doc: Discussions](https://docs.github.com/en/discussions)

[GitHub Doc: Issues](https://docs.github.com/en/issues)

## GitHub Pull Requests

A Pull Request is a workflow step that enables you to suggest a change to a project repository. The Pull Request, or PR, has become commonplace and so it is something to become familiar with. Pull Requests are not the only way to suggest changes but we are making use of this process since it is so common.

Very simply put, a Pull Request is a request for someone maintaining a GitHub project repository, to consider your changes for merging into the repository. This method allows for change suggestions from those not actively participating in development in a particular repository, and is also good practice so that changes made can be reviewed before merging and possibly breaking an actively-developed project.

Pull Requests include use of Repository Forks and Code Reviews and Discussions and are a way to synchronize collaboration without introducing too much confusion. A Pull Request can be somewhat complicated if you are new to collaborative project development, so please take a look at the GitHub documentation for Pull Requests:

[GitHub Doc: Pull Requests](https://docs.github.com/en/pull-requests)

## Attribution

It is a fundamental tenet of our organization, to attribute work done to those responsible. GitHub is a great tool for this, in cases where an individual commits work, whether it is new, or a modification of previous work (and whether it is code, or references to other works). The git and GitHub (and GitLab, and others) model assumes there is a one-to-one correspondence between effort and an official commit, but this is not always the case!

GitHub and GitLab (and to a lesser extent, git itself with external tools) support a Co-Author scheme, with references to collaborators included in Commit Comments in a structured way, so that these platforms will find and display the additional contributors to project commits (and thus, projects).

[GitHub Co-Author Attribution](https://docs.github.com/en/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors)

There are two important notes here:

1. The commit itself is still officially owned, and signed, by a single individual. This is not ideal in a future with collaboration being the norm, but it does make a reasonable assumption that a single *owner* of a new or changed element is responsible for it, with additional collaborators attributed explicitly. We will pursue this scheme and we will ask that all are careful to include collaborator attribution whenever it is appropriate.
2. There are some cases where an individual may not wish to share their email address, and in these cases GitHub (and possibly other platforms) offers an indirect email address option. As you can see above, the co-author annotation scheme is based on email address, and the email address used must be associated with a GitHub (for example) account. While using a platform-specific indirect email address makes it difficult to move repositories to other platforms maintaining the attribution, this is a useable method to accomplish private attribution. See this document for GitHub, and remember to use the preferred email address for each of your co-authors whenever you collaborate so that they receive proper attribution!

[GitHub Private Commit Email Addresses](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address)

## The End of The Beginning

There is far too much to talk about regarding Git and GitHub, this Howto is here to help you jump on board the Innovate for Vegas Foundation team and you will learn about this tool and more throughout your time participating with your team and projects. If you need help with any of these steps and suggestions above, do not hesitate to reach out at an in-person meetup or other gatherings or online, your colleagues are there to help. It is important that you are a part of a security-conscious and workflow-conscious cohort so that we can all make the most of our volunteer time and in so doing, learn valuable skills in areas of projects, project management, collaboration, experimentation, and of course the use of tools to shift your focus from mundane tasks to creativity!

Git is not perfect and GitHub has its issues, but they do most of what we need well enough that we can depend on them to get you and us much farther (and further) down the path than if we did not have them. Worth your time to check this stuff out, see some initial references below, and do not for a moment believe that this is the end of the learning.

## References

The theory of revision control, the history of tools that do this, how they are a part of project management and deployment workflows, and a whole lot more, can be found online in the form of tutorials, YouTube videos, articles, tweets, TikToks, and who knows where else. Git is everywhere, and GitHub has made an entire platform around it (and then Microsoft bought GitHub). There is also GitLab, and Atlassian’s Bitbucket, and many more, and you can always host your own git server locally if you want (or in the cloud somewhere).

So to get started, here are some links:

These are books, which are mostly non-free, but which may be helpful if you are completely new to revision control systems:
[Best Git Books of 2022](https://initialcommit.com/blog/best-git-books-2022)

An introductory deep dive by FreeCodeCamp on YouTube:
[Git and GitHub for Beginners - Crash Course](https://www.youtube.com/watch?v=RGOj5yH7evk)

This is an excellent reference manual and is worth bookmarking, though it is a bit dense to start with. Keep it handy:
[Git SCM Book](https://git-scm.com/book/en/v2)

There are many many resources out there, the most important one is right in front of you. If you have access to a computer, you can install git on it and try it out for yourself, you can test out branching and tagging, commits and merges, stashing your work for later, and, well, check that Git SCM Book for all of the possibilities. Git as a tool is difficult to master, but not so difficult to use, and with the user interface that GitHub created around it, git itself and the tools and interface that GitHub has wrapped around it should not be feared.

Who knows, you may find yourself using git for your own projects, for things as simple as notes, maybe your CV that can change over time, a personal website, and the possibilities are endless from there.
