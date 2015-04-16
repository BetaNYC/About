# Releasing Open Source 
Source: [Civic Commons Wiki](http://civiccommons.org/2011/01/be-open-from-day-one/)
Copyright - Creative Commons Attribution 3.0 Unported License

Often an organization wants to release their code as open source software, but doesn't know how. Below is a rough guide.

There are two general approaches, with a continuum in between. Neither way is right or wrong, it's just a question of your resources and needs:

### Throw it over the wall. 
You have some code, and you want to make it available because it might be useful to others, but you '''don't''' want an open-ended commitment to maintaining an active open source project.
 
### Create and run a sustainable project.
You want to open the code and then run it as an active project: accepting patches, soliciting code contributions, adding new maintainers, participating in user and developer forums, doing regular releases, etc.

You don't have to decide in advance which one you're doing, though it's good to have some notion of where you're headed.  The checklist for the initial code release is pretty much the same either way.

Note that even if you decide to maintain the code out in the open, you don't have to spend time responding to other people's questions unless you want to.  That is, **you open source your code, not your time** -- you don't have to decide in advance how involved your team will be in the public project.  You can put the code out there first, and then see what kind of questions people have.  If you decide it's useful for your team to engage with the community, then do so; if it's not, then don't.  People are still free to use the code.

The steps for the initial release will vary a bit depending on the project, but at a high level they look like this:

* **If you can, be open source from the start**. For new projects, start them off as open source from the very beginning, rather than planning to open them later. See [this post](http://civiccommons.org/2011/01/be-open-from-day-one/) for a detailed explanation of why this matters.

* **Make sure you own the code**. If a contractor is writing code, make sure the contract specifies that you own full copyright on their work product, and that you own it from the moment the first line is written, not from when it is delivered.
 ** Exception: If the contractor retains copyright, then the contract should specify that all their work is made available to the government under the open source license the project is to be released with.
 ** Exception: Or, in some cases, it may make sense for a neutral third-party to own the code. As long as the license is open source, the owner doesn't matter too much.

* **Reduce or eliminate proprietary dependencies**. How difficult this is depends on how the code was written, of course. In general, you want as few proprietary dependencies as possible (ideally zero), because the fewer there are, the more people can try the code. In general, a dependency on a proprietary online service (such as Google App Engine) is preferable to a dependency on proprietary local software, partly because the online services tend to be cheap enough that most potential users or developers can run an instance there without great procurement hurdles, and partly because service APIs tend to get cloned anyway -- at which point the dependency is just on the API, not the service, and is no longer truly proprietary.

* **Vet the sample data**. If your code comes with test data, some of that data maybe suitable only for internal use (e.g., names, phone numbers, email addresses) and would need to be cleaned out before the code is opened. In some cases, this can mean purging your version control history.

* **Vet the config data**. Internal projects often store local configuration data right next to the code. If you're going to release the code, they need to be separated. If the config data contains secrets (passwords and such), and you're opening up the version history as well, you may need to change all those secrets after separating the config data out.


* **Vet the code itself**. Your code may contain code copied-and-pasted from elsewhere, sometimes in violation of elsewhere's license. While this was technically a copyright infringement even when your code was only used internally, it becomes a much bigger deal when you distribute your code.

* **Vet dependency library license compatibility**. Proprietary dependencies are not your only licensing concern -- there may also be open source libraries whose licenses are compatible for use but not for distribution. Now that you're distributing the code, you may have to look carefully at the requirements of the licenses and make sure they don't interact in a bad way. For example, versions 1 and 2 of the [GNU GPL](http://en.wikipedia.org/wiki/GNU_General_Public_License) are not compatible with version 2 of the [Apache License](http://en.wikipedia.org/wiki/Apache_License). The licenses of code you depend on may affect the license you choose for your own code, or affect how your distribution is organized. (There is not space here to describe all the possible effects of license interaction; just get help if the situation is not obvious.)

* **Document**. People will want basic documentation on how to deploy and administer it, and how to use it. If your code does not have that documentation already, write it. It's also useful to have some documentation on hacking the code, especially if you intend to run it as an active open source project.  But don't let documentation perfectionism block your open source release!  It's okay to start with very rudimentary, placeholder documentation, and then continue to improve it after the release (in fact, it's a chance for outside contributors to get involved without having to write code patches).  Think of this step as being about showing potential users and contributors that you understand the need for documentation and that you'll be responsive to doc contributions -- not about actually having complete documentation.

* **Choose a license**. Specifically, choose a *standard* license.  The vast majority of open source software is released under one of a few standard licenses. Stick to one of those standards to save potential users (and contributors) a lot of time.  Even so, the process of deciding which one can be somewhat involved, especially for governments, and may require the involvement of lawyers; see [[Choosing a License]] for details.

* **Apply the license**. Once you've [chosen a license](), applying it to the code is a fairly mechanical process, documented [here](http://producingoss.com/en/license-quickstart.html#license-quickstart-applying).

* **Package the code in a standard way**. Package the code so it is easy to deploy on the platforms it is meant to be deployed on. This might mean a standard source distribution (e.g., a Unix .tar.gz file), or a Microsoft Windows self-installing .exe file, or something else. Whatever it is, make sure that there is an automated process for going from the development source tree to the standardized distribution package.

Now the code is ready to be distributed. It's time to decide whether to just throw it over the wall or run an active open source project.

Throwing it over the wall is easy: just put the source distribution up on a web server somewhere (or check it into a public version control repository such as [GitHub](http://github.com/), [SourceForge](http://sourceforge.net/) or [CodePlex](http://www.codeplex.com/), after reading the advice on hosting [[Open Source Development Guidelines|here]]) and

* **Announce** the release in the appropriate places.  Generally, the way to do this is to write one canonical announcement and post it in some place that makes sense: your agency's blog, for example.  That piece should describe what the software does, include any important quotes, state that the code is open source (and specifically which open source license), and link to the project site, any demo sites, etc.  Then in each of various forums where people might be interested (e.g., Drupal discussion lists if it's a Drupal module, etc), do a shorter post, pointing out that the software has been released, and directing people to the canonical announcement for more information.  Keep those short and simple: the goal is to get people to read the main post and then come check out the software, not to get them follow up to your announcement with their own posts.

At this point, in theory, you could then walk away.

But if you don't want to walk away from a now-public project, the next thing to do read is [Open Source Development Guidelines]().

This document is forked from Civic Commons' wiki on "[Releasing Open Source](http://civiccommons.org/2011/01/be-open-from-day-one/)."

