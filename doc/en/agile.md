<!--
 Copyright (C) 2023 Innovate for Vegas Foundation
 
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

# Agile for Volunteers

Agile methodologies were developed by software developers for software developers and the infrastructure in which the business of software development takes place.

The [Agile Manifesto](http://agilemanifesto.org/) is the fundamental description of what Agile was conceived to be; we can start with one slight modification here:

> - Individuals and interactions over processes and tools
> - Working *projects* over comprehensive documentation
> - Customer collaboration over contract negotiation
> - Responding to change over following a plan
>  
> That is, while there is value in the items on the right, we value the items on the left more.

We can focus on a whole-team approach across project and project focus areas, rather than considering only the software parts. A project may include zero software, but we may attempt to follow Agile methods in developing that project nevertheless.

To be clear, at the time this document was created, Agile in this base form is typically applied in a business setting with employees or contractors, collaborating with their customers and business interests, and management layers, to advance a project along a timeline, through iterations, to achieve a goal or goals along the way. Our approach will begin here, but because we are an all-volunteer organization, we may need to adapt. In fact, we shall do precisely that.

## Specifications vs User Stories

One of the core principles of Agile is to factor development into independent components and progress through these components to advance toward a completed form of the overall project. The project itself will almost certainly go though an evolutionary development cycle over its lifetime, but at any given time the features that are the project, from the customer point of view, are described as User Stories, to provide context and loose definition for those implementing the pieces.

In our overall infrastructure scheme, the ov- repositories in GitHub, which are Project Overview components, fill the role of loose specification and the starting point (and storage location) of the User Story Backlog. In the early days of a project lifecycle, there is no code (or very little), likely no visualization, no content, no artwork… nothing. The Project Overview is a starting point with a specification that is mostly normative, in that it is describing at a high level what the project could or should be, and what the top-level parts might be, but this is not to be taken as the final roadmap for any project or project component.

The User Stories, in keeping with the Agile method and workflow, are where we begin to spell out what a User might expect, in a more granular, detailed way. While the ov- specs provide a big-picture, there is no intention to make the description of the project parts there, the actual parts to create and assemble. This is where User Stories come into play, and even then a User Story is a more specific guide. Ultimately the individuals implementing project components (the User Stories) collaborate with peers, other members of related teams, and customers, as development of the project and its components proceeds in a collaborative and iterative journey toward elements that do what they are supposed to do.

Does this sound vague? That is okay, because volunteers are not putting in 40+ hours per week in exchange for a paycheck, and as empowered members of a project team (or teams), each individual contributor plays a part in crafting what we implement.

## Customers

Use of the term *Customer* may seem odd if you believe a customer in the context of a project is similar to a customer in a retail business setting. This is not always the case (though sometimes it is).

If you are working on a part of a project, and another individual or team depends on your work, they are your customers. If your progress depends on the work and progress of another individual or team, you are their customer. If a person who uses Smart Calendar features needs to use an API, view a Calendar webpage, or use these tools in other ways as a programmer or as someone who needs to know where they are going and at what time, these are customers. A customer has needs and expectations, and the are understood and addressed through a collaborative effort that includes comprehension and communication, along the development process.

### Internal Customers

As mentioned, your customers may be fellow volunteers working on related project components, so that the collaboration process may be easier, or move more quickly, because we may all be working in familiar territory, we may know each other, and we may have the overall goals (the Capstone Project and its various related component projects, for examples) mapped out for all to see, making our individual contributions a bit easier to understand and communicate.

Working with our internal customers will provide opportunities to collaborate more closely than we might with external customers, so that someone working on one project (a customer of yours) could collaborate with you on solving a problem, implementing a feature, changing some details… they are part of your team, and we can take advantage of a whole-team approach with serious wins!

### External Customers

As our projects become more visible, they will capture the interest of municipal partners, other open source developers, and perhaps most interesting, our friends and neighbors in our communities around us. As we Make our Smart City Smarter, it makes sense that we involve our customers in the process so that what we develop can meet their needs, and maybe impress them a bit. This is how volunteer efforts become shining examples of work completed on your CV, and maybe even actual jobs, whether for other companies, or your own.

External customers are more likely to guide the loose Specification and User Stories described above, without joining in on actual project work we we might internally. Still, a customer wants or even needs what you are working on, and as a responsible professional, one of your goals should be to meet or exceed those expectations, and keep your External Customers in the discussion along the way as much as they can be, though probably not quite as much as you can with Internal Customers.

### Co-Creation

Sometimes a *customer* is not going to be quite so closely involved with specifying project components are developing User Stories in a structured way. However, anyone who needs or wants what we are working on will tend to have an opinion or feedback, or maybe a good idea that we had not considered, or a bad idea that we should not consider. If we use the more familiar definition of *customer* you had in mind before you read this section, then you have almost certainly encountered an unhappy customer who would be happy if whatever it is they want or need would work the way they want or need it to. If only there was some way for the customer to talk to the people making this thing, the fix might be obvious, or maybe it is more subtle, either way it is all too common for customers to become frustrated with their wants and needs ignored. We can tackle that.

You can visit this article, [Co-Creation](https://www.interaction-design.org/literature/topics/co-creation) and find this serviceable definition:

> Co-creation is the practice of collaborating with other stakeholders to guide the design process. Participants with different roles align and offer diverse insights, usually in facilitated workshops.

Our Internal and External Customers are stakeholders, but so are the people you have never met and may never speak to or interact with directly, but who have those wants and needs. Can they participate in the process we are describing here? Absolutely. Are they always enabled to do so? Well, we are going to make that a priority.

Elevating our community is one of our goals, including our community in our efforts is a win-win proposal.

## Iterations (aka Sprints)

The typical Agile workflow, in whatever variation you may have come across it or participated in it, involves the assumption that participants are working on their stories (or open issues, backlog, etc) on a regular basis, reachable for stand-up meetings, collaborative discussions, pair programming, ideation on a design idea, and so on (coding or creating, it is a question of focus). In our Volunteer Agile scheme, we cannot possibly depend on consistent and predominant attention, focus, and effort. The path to completing iterations will not benefit nearly so much from tuning of expectations and work progress. Since we are not a software company, our open source projects can proceed without the pressure of release dates and milestone constraints.

However, our internal customers are probably your fellow customers, and other people working on your project, possibly as a part of your team, and while everybody involved might be a volunteer, it is important to remember that *everybody else* is also a volunteer, which means all involved must arrive at commitment consensus. As part of a team, your effort may add to the effort of others, while your lack of effort may subtract from theirs. As we move through each successive iteration on a project timeline, we will all learn what individuals and teams can accomplish together and at what rate. This helps set expectations not only for Internal and External Customers, but also for the other members of your project team, and for yourself.

The specifics of Agile Iterations are beyond the scope of this document, and given the challenges of coordinating volunteer time and effort, we will probably need to collaborate and experiment a bit with what works and what might work better. A potential starting point might be to set an iteration time interval (2 weeks? 4 weeks?) and then find out what each contributor can accomplish one step (or story, issue, etc) at a time through the interval, without committing to that level of effort in succeeding iterations. This section will receive more attention and updates over time, at the moment we will assume experiments first and then write things down later.

## Integration

Whether you are developing software or working on content or designing logo or user interface elements, or any of a myriad of items that make up a real project, you will most likely need to make what you have completed fit into the project with the work that others have completed. Sometimes, changes take place in small ways here and there, but which add up to a system that suddenly does not work. We need to avoid that, because volunteer time is difficult to come by, and we should try to spend it on progress, not error correction.

### Intra-iteration

Through each iteration interval, the members of the iteration team need to commit at the very least to finishing and submitting the parts they take on back to the project and making sure everything still fits together. In other words, it is going to cost time and effort of others any time a start does not include a finish, even for small tasks and certainly for larger tasks, so it is important to, at the very least, complete even one of the issues or stories you commit to working on, integrating it back in to the project for that iteration.

Anyone who is actively participating in an iteration can, and should, integrate their work directly into the project. This applies to code, and any other project elements (not only the coders, but everybody!), and so members of a team should consider their efforts subject to continuous integration through the iteration interval. By integrating continuously, and testing your changes before and the integrated outcome after, you can be a part of advancing the project forward.

### Extra-iteration

Contributing to a project outside of direct participation during a project iteration is possible, and probably appreciated, but since such efforts are made outside of the iteration interval, it is unlikely that a continuous integration approach will lead to satisfactory outcomes. Here, a better approach is to submit a patch, or in the case of a GitHub project repository, a Pull Request, which can be considered during or after the project iteration interval.

By way of example, a suggested change to a piece of artwork or other content element(s) by an internal or external customer, fellow open source developer from parts unknown, or anyone else, can be submitted to the project team any time, with integration at their discretion, which might include rejection outright. Similar criteria are assumed as in the Intra-iteration scenarios you may encounter, except that the Extra-iteration contributions may or may no fit into the Iteration goals, or they may not work at all. Or they may be perfect.

## Whole-Team, Pairing, and More

The whole-team approach in Agile encourages collaboration across project components for which the whole team participates and is responsible. *We are all in this together*, if you like, which leads to some other useful side-effects:

- Shared responsibility implies backups of familiarity, since if one person is unable to complete a part of a project, for whatever reason, at least one other person is familiar enough with that component to fill in, and possibly complete that component.
- While individual contributors take ownership of particular tasks and user stories and issues in general, pair and mob collaboration is always encouraged and usually adds tremendous value not only to the project, but also to the team.
- Since we are extending our Agile umbrella to cover coders *and* creators, it is entirely possible that a coder will become a more capable logo designer or media editor, while a visual artist or content creator might learn how to code. Cross-functional collaboration across these boundaries make them not-boundaries.

### Atomic Teams

In order to adapt the Agile Iteration model to our Volunteer cohort structure, we will attempt to make Teams atomic for iteration time intervals, so that during a particular iteration, it may be possible to rely on the application of the whole-team approach to a subset of the overall project, as usual for a sprint, but with the Team technically disbanding at the end of an iteration (and possibly re-forming in whole or in part for the next iteration). There is no guarantee this will work well, or work at all, but it is one way to accommodate a volunteer cohort where predictable, regular, and recurring participation as one might expect in a more traditional workplace or general work environment cannot be guaranteed.

To make the most of whole-team benefit, we say that the Team is Atomic during the Iteration to set expectations across the Team, that those starting the iteration on the team will end the iteration on the team, having attempted to complete, or at least make progress on, the parts of the project each claimed for work during the iteration.

### Attribution

During each iteration, our whole-team approach benefits the project *and* the team, and our stated policy is to always enable full and transparent attribution of all contributed creative works to all the right person or people who made those contributions. This is something that happens frequently in the world of software development, particular with pair and mob programming during Agile Iterations, but we want to make sure that non-code creative work is also correctly and consistently attributed. Credit where credit is due!

As of this writing, our Foundation is making frequent and fundamental use of the GitHub platform to keep track of our projects, which includes contributions of creative works to those projects, with attribution. We will develop best practices and if possible, integrations with tools and platforms that are integral to the creative work development process (one example might be the use of Figma, but where outcome of collaboration using that platform is captured in a project component repository, with attribution to authors and co-authors) so that we can present a consistent, transparent interface to anyone interested to know who made their favorite bits possible.

[GitHub Co-Author Attribution](https://docs.github.com/en/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors)

Using this scheme described, it is a small matter to make certain that collaborators get credit for their work and effort, which may well be pivotal. The work still has a primary *owner* and in cases where there is only one contributor, or two, or ten, or more, the owner of the bits owns the commit. However, adding the Co-Author trailing data in commits provides that transparency in a generally accepted an mostly-cross-platform-compatible way.
It is important to be attentive to including this information when changes and additions are committed to each project repository, since adding this information later becomes difficult, and since giving credit to collaborators should become second-nature, something you are unlikely to forget to do when you develop that muscle memory!

## Stand-ups and Meet-ups

One of the core human principles of Agile is the notion that co-location and frequent interaction is a net win at every turn, from enabling spontaneous or more-easily-scheduled collaborations to casual off-topic conversations to general team building and cementing cross-function familiarity over time. In a formal workplace, or even a virtual workplace in interesting times or with remote participation as a norm, daily stand-up meetings are easy to integrate into a work day and the project workflow.

In the case of a team of volunteers, even if that team is atomic for an iteration interval, it is far more difficult to ask for, and receive, a daily time commitment for stand-up meetings, however brief. It is reasonable to have monthly project meetups, but month-long iterations are almost certainly too long to maintain attention. As a first guess, iterations should be about 2 weeks in time, with sync meetings at the 1-week mark (assessing progress, adjusting and tweaking and whatnot), while a monthly meetup could be used as time to work in person and work on project planning across various projects and project components.

We can encourage project teams to meet when they can, at some geographically convenient location at times that work for pairs or the whole team, or online with chat or screen sharing or other forms of collaboration that enable interpersonal engagement along the way.

This component of Agile, for our applications, will most likely prove to be the most challenging to get right, with the largest opportunity for return on investment against the highest barriers.
