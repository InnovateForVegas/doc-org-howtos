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

# Specifications and Documentation

In the context of our Foundation Entities, the *Overview* repository for each Initiative includes specifications, or more correctly a Bluesky Purpose document collection, for that Initiative, and then there are one or more *Documentation* repositories.

What is the difference?

First, let us establish two definitions:

**Normative** is used to describe things the way they should or might be. Literally leading to or related to establishing *norms*. In fact, if you encounter a statement with the word *should* in it, for example, this is a normative statement.

**Authoritative** is used to describe things the way they actually are or must be, and an authoritative statement is intended to be accurate and correct.

## Normative Overviews

When we create an overview repository and the content within, we are creating a Normative description of what we intend to do, captured in our Bluesky Purpose document collection. Which challenge we intend to address and how we intend to solve or improve or overcome it? Of course these could be plural, since any initiative will likely have several interlocking and disparate component projects. Much like the tried-and-true Scientific Method, we have our problem statement, and we have a hypothesis which posits how we will implement project components to see if we reached our solution. Simple!

Not really. As with the scientific method, our hypothesis might lead to failure. However, failure is simply more data to feed back into our methods. We can always adjust our overview with additional and update specifications or possibilities in our Bluesky documents, and we can refer to any issues and discussions (in the GitHub scheme of things) built up along the way, on which to base our updated hypothesis. Normally technology projects at our scale will simply roll through the iterative process, with the parts of the Initiative or specific Component Project that are not working either dropped completely or altered to fit better. This is the nature of fixing bugs and releasing new versions. For non-technology projects, the same still holds, though often the iteration and improvement process is different; if a logo or other visualization is not clear, for example, it may need to be revisited and changed, but one does not simply release a new version and call it a day.

At any given time, our project overview should reflect what we would like the project to be, what we would like for it to do, and in general, indicate what its outcomes *should* be. As we move forward with our [Agile for Volunteers](agile.md) initiative and its methods and workflows, we will find that our Overviews will be much more useful if they are adaptive and flexible as we collaborate and capture feedback from our customers, and our peers.

## Authoritative Documentation

When we create a documentation repository for an Initiative or Component Project, we intend to inform a user or consumer or perhaps another developer of what this Entity does, how it works, and what to expect. The Entity documentation eventually evolves into product or service documentation, which is where someone might look to determine what this thing does. They should be able to obtain correct and accurate answers, and so our documentation is intended to be authoritative for any particular release or version or iteration of a project component.

This is why documentation repositories will need to track the Entity (Initiative, Component Project, etc) they are attached to, but can not really lead them. Perhaps a *To be implemented* section is useful for some, but in general the documentation should be about the here and now, not future versions and their features and fixes. That is what the overviews are for!

Note that our overview repositories contain the Bluesky Purpose documents (which are *normative*) as well as documentation where applicable. Our normative specifications will almost certainly refer to external projects and specifications for protocols and formats, and these should be *authoritative*. Thus our overview repositories will contain our Entity as it should be, with references to these external components as they actually are. If you have ever heard or read something like “developing against a moving target,” this can happen with the external components are still changing and have no authoritative documentation for some released version (there are more examples of this, if you find yourself tracking a changing dependency you will recall this mention).

## Internal vs External

Since we touched on external dependencies for our projects, we can end on the difference between internal and external dependencies and how they impact our Initiatives and progress.

They are essentially the same.

If a particular Component Project or external project or product is a requirement for a project component you are working on, you will sometimes encounter incorrect documentation, or so-called *undocumented features* which may cause strife or delay or other issues to consume your time and effort. The dependency may be on something from some other organization (a company, an individual, some open source or closed source element, etc), or it may be on a project component from another volunteer team within our Foundation. In the case of the former, you may have to wait, or proactively reach out for a fix or update, perhaps with a suggestion or even a pull request or similar if that is something you feel comfortable doing. In the case of the latter, since our Foundation Entities are all Open Source and intended to be the sum of time, effort, and expertise of our Whole Team of Volunteers, you can do exactly the same thing, and perhaps you will know exactly who to address your pull request to…

Another difference between internal and external components is, you are always welcome and encouraged to contribute to the Bluesky Purpose documents and Documentation of our internal projects, and in a perfect world your contributions there will correspond to features and fixes and in general a better outcome than you found. This is the purposes of the Agile for Volunteers workflow, where the Bluesky Purposes is transformed into what we intend to build or make or otherwise develop. External components are often less open to taking your suggestions, which is reasonable for anyone working on any project anywhere with suggestions coming in from others whom they do not know. In any case, though, the next time you are writing or updating a specification anywhere, or adjusting project documentation, consider who will be benefiting from your work and how their work benefits you!

Part of our [Agile for Volunteers](agile.md) Initiative will highlight the Internal vs External customer side of things, this will all become more clear as we practice and tune our workflow and collaborative methodologies.

# References

[Normativity on Wikipedia](https://en.wikipedia.org/wiki/Normativity)

[Authority on Wikipedia](https://en.wikipedia.org/wiki/Authority)

[Scientific Method on Wikipedia](https://en.wikipedia.org/wiki/Scientific_method)
