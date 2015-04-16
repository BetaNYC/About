# Running an Open Source Project / Open Source Development Guidelines
Source: [Civic Commons Wiki](http://wiki.civiccommons.org/Open_Source_Development_Guidelines)
Copyright - Creative Commons Attribution 3.0 Unported License

This is a checklist of things to think about for running an open source project, focused on the particular challenges faced by civic entities.

It discusses what collaboration tools are needed, how to attract and incorporate new contributors, how to handle both volunteer and paid (vendor) contributors simultaneously in the same project, keeping legal ducks in a row by getting contributor license agreements when needed, etc.

For guidelines on doing an ''initial release'' of open source code, see [[Releasing Open Source]] -- and then come back here.

<span id="hosting" title="hosting">
*'''Host in a standard place, and run the project there.''' Use standard public hosting infrastructure as much as possible (e.g., for bug tracking, version control, discussion lists, etc), and make sure that that's where primary development work actually happens.  Example sites: [http://github.com/ GitHub], [http://code.google.com Google Code Hosting], [http://sourceforge.net/ SourceForge], [http://gitorious.org/ Gitorious], etc.  Or, if your software is part of an existing community (e.g., it's based on [http://drupal.org Drupal] or some existing code base) and that community has a standard hosting service for add-ons and modules, then host there.  Note that even in cases where it's absolutely necessary, for political or other reasons, to violate the "[http://civiccommons.org/2011/01/be-open-from-day-one/ Be Open From Day One]" rule, it still makes sense to host privately on a standard hosting site if possible and then open up the code when ready.  Although private hosting often costs money, while public hosting is free, it will still cost less than hosting it yourself.
**Justifications:
***Standard infrastructure makes it easier for others to interact with the project without bothering your team with questions; it also makes it easier to bring new developers in, as employees or otherwise. The farther from those collaboration standards you drift, the more overhead you incur in maintaining and explaining your hosting situation.
***You get upgraded automatically.
***It's in keeping with the "[http://www.cio.gov/pages.cfm/page/Vivek-Kundra-Testimony-on-Cloud-Computing cloud first]" recommendation for the Federal government
**Use an organizational account name that reflects the office, not a person.&nbsp; For example, New York City uses the "[http://github.com/CityOfNewYork "CityOfNewYork" account]" on GitHub.&nbsp;  Consider using a role-specific email address too, like "opensource@your.department.gov", so the project hosting accounts do not need to be updated when personnel changes happen.
*** '''If GitHub, make sure to use an _organizational_ account.''' Your developers will send and receive code changes via their individual accounts, as members of the appropriate organizational account.  If you don't know about the latter, or you need to convert your city's individual account to an organizational account, see [[GitHub Organizations]].
**Register the ''same'' account name at at least the first three project hosting sites above.&nbsp; You may only use one of them for now, but you want to have a consistent namespace in case your office changes its mind later.
**Note: There is no issue about the government entity receiving a "free gift" by using one of the public hosting sites, because those sites offer their free services to everyone on the same terms. There is no favoring going on.
**We've heard about a GitHub study on how contributions to Mozilla went up something like 600% after they started hosting at GitHub. ''(Citation needed, of course.  Would be great to find this and link to it from here.)''
</span>

*'''Have discussions in public.''' Keep non-private discussions on the public lists as much as possible; use internal forums only for things that actually need to be private. When interested parties ask questions, direct those conversations to the list, so others can see.
**Justification: Even though there might be no one besides your developers on those lists at first, the archives will be valuable later -- they're a knowledge base in which others can dig up answers without bothering your team.
**See the section on "Mailing lists / online message forums" below for technical details on how to set up this kind of environment.

*'''Open your code, not your time.''' Your team isn't obligated to engage outside inquirers -- you should do so only insofar as it helps the project (which it sometimes does, since outsiders often spot problems, raise important design points, have development resources to offer, etc).
**Justification: Sometimes managers are afraid that open sourcing will mean their team gets bombarded with questions, and has to spend too much time answering them. In practice, it's unlikely that this will happen to your project anyway, but it helps to be clear in advance that you're not open sourcing your programmers' time, you're just open sourcing the code.

*'''Invite inspection, but don't count on it.''' Invite security reviewers in early -- don't count on the "many eyeballs" effect to provide free security review. Especially if your code will run on government servers and hold sensitive information, particularly about citizens, then it's important to make sure it's secure.
**Justification: This is really independent of the code's being open source or not. But sometimes people think that exposing the code to public scrutiny means security holes will be found. It isn't a guarantee, though; you still have to take complete responsibility for security.

*'''Have a procedure for incorporating code contributions.''' When incorporating code from outside contributors, get a clear assignment of copyright or a statement that the code is being released under a compatible license.  See [[Contributor Agreements]] for details.
**Justification: this is true for all open source projects, but it's particularly important for government projects because it can be very embarrassing for your jurisdiction (and hence for your boss's boss) if code gets in without clear ownership. (This is unrelated to technical vetting, which should be a matter of course.)

*'''Make sure partners are on board with all this.''' If a contractor is involved, make sure they're completely on board with producing and running an open source project.
**'''Credit partners accurately, including contractors.''' Credit is independent of licensing: any contractors should be accurately credited for the work they do. This is both standard open source practice and good business for both sides.

*'''Put a commercialization strategy into any RFPs.''' Commercialization of open source code should be considered a benefit and be encouraged. When contractors bid to develop open source software, they should be asked to include a commercialization strategy that takes advantage of the software's open source nature.
**'''Outside help is fine.''' For many established contractors, especially large ones, open source is a new world. When necessary, be willing to engage third-party help, either directly or as a subcontractor, to guide them through this process. (Example: VA contracted with a NJ company to help them with the Vista open source process.)
**'''Commercial is not the same as proprietary.''' Commercialization does not mean making a closed-source derivative fork of the software and reselling it. An open source commercialization strategy is built around the continued development and deployment of the open source code.
**'''More players means more pie.''' A commercialization strategy that involves attracting ''more'' vendors is better than one that attracts fewer.

*'''Include a followup step.''' At maybe 6 months and 1 year post-release, build in an evaluation, preferably by a third party: is the software still effectively open source? Are there outside contributors? Did any kind of vendor ecosystem spring up? Are there still obstacles to any of these things? As one correspondent pointed out: there are a million ways to subvert procurement or contractual requirements, so one can find ways around mandated open source too. &nbsp;E.g., "Hi, we open sourced it just like you said, too bad we only wrote the code to run on this specific chip that we own the tool chain for".

''The items below should be expanded to discuss specific qualities government projects should look for in these collaboration tools, or should take advantage of.  The most important one is probably APIs.  For example, when choosing a hosting site, GitHub's version control system, git, automatically comes with a perfectly complete API, supplied by the git client itself.  On the other hand, at least as of 2011-09-01, their bug tracker does not seem to offer any API beyond the browser-based user interface, whereas Google Code Hosting's bug tracker does offer an API.  These are important considerations when it comes to soft lock-in; it may even make sense for projects to use the version control repository from one service but the issue tracker from another.''

<span id="discussion-forums" title="discussion-forums">
*'''Mailing lists / online message forums.''' If you don't have a better mailing list / discussion forum solution in mind, [http://groups.google.com/ Google Groups] will do the job.  Whether you use Google Groups or some other system, set it up this way:
** Anyone can read the archives online, without having to log in.  Anonymously browseable archives are key, because it is often through browsing the archives that a person decides whether or not to join the discussion group and become more active in the project.
** The archives should be searchable.
** The archives should also be indexable by major third-party search engines such as Bing, Google, Yahoo, et al.  When people go to one of those search engines and enter a query about your project, you want relevant posts from your discussion forums to be eligible results.
** To prevent spam problems, set up the posting controls like this:
*** Posts by non-members (i.e., anon posts) are either disallowed or always moderated;
*** Joining the group (i.e. becoming a member) itself can be moderated, though if you expect a lot of people to join in a short period of time, and don't want to worry about moderation delays, then you could allow open joining for a time;
*** First post by a new member is moderated, and thereafter that member can post without moderation (if they start behaving in a spammy way, the moderators can take special action, but this is rare).
** If you prefer not to use Google Groups, some other options are: [http://sympa.org/ Sympa], [http://resubj.com Re:Subj], [http://librelist.com/ Librelist], [http://coactivate.org CoActivate], [http://onlinegroups.net OnlineGroups.net].  You can also host discussion groups on your own server using [http://groupserver.org/ GroupServer] (also offered as a hosted service at [http://onlinegroups.net OnlineGroups.net]), [http://list.org GNU Mailman], or [http://ezmlm.org EzMLM].  We recommend trying GroupServer; Mailman and EzMLM were state-of-the-art years ago, but nowadays they do not have all the features one wants in discussion forum software.
** See http://producingoss.com/en/mailing-lists.html for more on the social and technical aspects of running discussion forums.
</span>

*'''Version Control''' These days, the default choice for open source projects is to use [[http://git-scm.com Git]], with master code repositories hosted on [http://github.com GitHub] (see [[GitHub_Organizations here]] for more).  However, if the developers are already using some other version control system (e.g., [[http://subversion.apache.org Subversion], [http://cvs.nongnu.org/ CVS], [http://mercurial.selenic.com Mercurial], etc) and don't want to switch, that's fine.  The most important thing is that the developers be happy, so if they want to use something other than Git, let them.  Just make sure that the version control system itself is open source (otherwise you'll be locking out potential contributors and adopters).  There are free project hosting sites for all the major version control systems -- in fact, GitHub is unusual in offering just one (Git).

*'''Bug Tracker''' Track bug reports publicly.  If the project was developed in a closed-source manner before being opened up, then you may have an in-house legacy bug database already.  Export those bugs over to the public tracker and shut down the internal tracker if you can -- but if that's too hard, then use a two-step process: file all new bugs in the public tracker, and whenever someone starts working on a bug from the old tracker, transfer the relevant parts of the bug report to the new tracker, close the bug in the old tracker (leaving a forwarding pointer), and track it in the public tracker from then on.
** You don't have to use the bug tracker offered by the hosting site where you host your code, wiki, or other resources.  You ''can'', if you like that tracker, but it's perfectly fine to use a tracker somewhere else -- even at another hosting site, if it has features you prefer.
**However, hosting sites often integrate the bug tracker with the hosted repositories, wikis, etc.  For example, if you commit a code change with a message containing "Closes bug #567" then the bug tracker ticket will automatically get a comment added referring back to that commit.  This integration can be very convenient, and should be weighed
**Some features to look for:
***Email interaction: some developers really love it when they can interact with the bug tracker by email: receive notifications, file new bugs, and add comments or responses on existing bugs.
***APIs.  If you can interact with the bug tracker programatically, then your developers are not limited to the web-browser user interface provided natively by the tracker, and they can write scripts to parse and analyze bug activity.  The [http://code.google.com/hosting/ Google Code Hosting] platform's bug tracker has APIs; others may as well.
***Easy import/export.  Prefer a bug tracking system that has an easy way to export bugs, either via an API or at least via an "export" button.  That way you're not locked into whatever choice you make.
**See [http://producingoss.com/en/bug-tracker.html this list] of bug tracking systems for more.

*''Other technical infrastructure to offer:''
**'''Wiki.'''  Enough said.
**'''Live chat room / IRC.''' Create a channel at [http://irc.freenode.net irc.freenode.net].  See that site and [http://irchelp.org IRC Help] for more information.
**'''Demo site.''' Providing live demo sites of your software in action is even better than screenshots.
**'''Development servers.''' If the software is difficult to set up a development environment for, and you have some resources, consider setting up dedicated development servers (as re-imageable virtual machines) that you can give contributors access to on request.

=Other Resources=
* [http://ben.balter.com/open-source-for-government/ Open Source for Government guide by Ben Balter]
* [http://wiki.civiccommons.org/Legal_Policy#Chapter_4_-_Legal_Issues_and_Best_Practices_With_Starting_a_New_FOSS_Development_Project_In-House Civic Commons' Guide to Legal Issues to Developing Open Source Software in Government]
* [http://mako.cc/projects/howto/ Free Software Project Management HOWTO], aroughly 40-page pamphlet
* [http://producingoss.com/ Producing Open Source Software], a full-length book.
* [http://contributing.appspot.com/ Contributing App] is a lightweight application/website that's used to provide a baseline of information about an open source project, so that if it gets abandoned, there's enough information for someone else to take it over -- which makes it also a pretty good overview of the bare minimum needed to have (or revive) an open source project.

''Other topics that should be covered here (like all wikis, this one is always in progress):''

*''Installation / deployment documentation.''
*''Announcing.'' Announcing the release in the appropriate forums.
*''User documentation.''

==Open Questions==

*The above is all more about a government entity starting an open source project than contributing to an existing project. The latter might need different recommendations.  There's a separate set of recommendations to be made about how when you use open source code, you should try to push useful improvements back upstream... but in practice, I'm not sure how worthwhile it is to spend time on that. It's a recommendation that programmers adhere to when they have time & resources to do so, and ignore when they don't; this is as true in the government as in the private sector.


[[Category:Open Source|Open_Source]]
[[category:Guidelines]]

Copyright - Creative Commons Attribution 3.0 Unported License