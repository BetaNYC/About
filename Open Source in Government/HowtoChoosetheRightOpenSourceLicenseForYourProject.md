# How to Choose the Right Open Source License For Your Project
Source: [Civic Commons Wiki](http://wiki.civiccommons.org/Choosing_a_License)
Copyright - Creative Commons Attribution 3.0 Unported License

Although there are many open source licenses List of [OSI Approved Licenses](http://www.opensource.org/licenses/alphabetical), the important ones can be divided into two categories, and within each category only a few licenses are in widespread use.  Note that open source licenses include strong disclaimers of liability -- this is something virtually all of them have in common, so you don't have to look for it specially.

## The "Anything Goes" Licenses

These place very few restrictions on what can be done with the code, including using the code in proprietary derivative works. They require only attribution in a specified manner. The most widely-used licenses of this type are:

* [BSD-style](http://opensource.org/licenses/BSD-2-Clause)
* [MIT/X11-style](http://opensource.org/licenses/MIT)
* [Apache Software License, version 2](http://opensource.org/licenses/Apache-2.0)

## The Copyleft (so-called "viral") Licenses

These also allow open distribution, modification, and re-use of the code (with attribution), but insist that any derivative works be distributed under the same terms. Thus proprietary derivatives by third parties are not possible (unless the copyright holder gives permission).  Note, however, that commercial use and derivation by anyone is permitted, as long as the terms of the license are honored. Widely-used licenses of this type are:

* [GNU General Public License, version 3](http://opensource.org/licenses/GPL-3.0 GPLv3)
* [Affero GPL, version 3](http://opensource.org/licenses/AGPL-3.0 AGPLv3)
* *Note* that the AGPLv3 is essentially the same as the GPLv3, with one additional clause that requires source code distribution (under the AGPLv3) to those to whom the software is exposed as an online service.

## What About the Public Domain?

This isn't really a license, it's just an explicit disclaimer of intention to enforce copyright. A standard way to make such a disclaimer is to use a recognized text (for example, the [CC-0](http://creativecommons.org/publicdomain/) dedication). We don't recommend public domain for distributing open source software, for various reasons (absence of liability limitation, the fact that not all international jurisdictions even *have* a clear public domain, etc). However, sometimes software produced by the US federal government must be in the public domain by law. Note there are some open source packages that deliberately chose to be in the public domain (e.g., [SQLite](http://sqlite.org/copyright.html)) and it doesn't seem to negatively affect their adoption or their health as open source projects.  However, we recommend against public domain if you can avoid it; it's always better to use a standard open source license, for reasons of legal clarity and for consistency across national boundaries.

The Open Source Initiative's [FAQ item about public domain software](http://opensource.org/faq#public-domain) gives more detail about this question.

## So Which License Should I Choose?

It depends on what effect you want. If you're comfortable with companies coming along and using the code in possibly proprietary products (that they will then try to sell back to you), then just use the BSD-style license from "anything goes" category, for these reasons:

* It's short and simple, hence easily comprehensible by lawyers evaluating it to know if their jurisdiction can use the software.
* It's compatible with all the other licenses. That is, code licensed under a BSD-style license can be mixed freely with code under any other license. (Importantly, it is compatible with older code under GPLv2 as well as the newer GPLv3; the same is not true of the Apache License, which would otherwise be a good choice.)
* It avoids controversy. While there are arguments in favor of using a copyleft (second category) license, doing so would look like taking a position in various internicine debates popular among open source and free software advocates. By using a BSD-style license, the software will be just as free, but you can avoid getting drawn into such debates.

On the other hand, if you *don't* want proprietary derivatives from other parties appearing, then use a copyleft license: the GPLv3 or the AGPLv3. The latter is preferable mainly if you want to ensure that anyone offering hosted instances of the software on a network makes their source code available (with their modifications, if any).

Note that the AGPLv3's special provision regarding online access can be problematic for some government organizations: they may wish to host publicly accessible instances of the software, and yet be unable (for regulatory or security reasons) to release their own customizations to it in a timely manner when asked. If that's a concern, but you still want a copyleft-style license, go with GPLv3. The plain GPLv3 is also very widely recognized -- including its earlier v1 and v2 incarnations, it's the most widely-used open source license there is -- and that familiarity is an advantage in itself.

## Dual Licensing

Copyleft licenses like GPL and AGPL (see above) are also sometimes used by vendors as part of a [dual licensing](http://en.wikipedia.org/wiki/Dual_licensing) business model, whereby they release the code under a copyleft license, but can also sell per-copy exclusive licenses to organizations that want to use or redistribute the software under proprietary terms.

Note that "proprietary" is *not* the same as "commercial".  Commercial use is already permitted (to all parties) by all open source licenses [The Open Source Definition](http://www.opensource.org/docs/osd), and this right does not go away in a dual-licensing arrangement.  "Proprietary" is different: it's when a licensee wishes to redistribute the software (perhaps as part of some larger offering) under non-open-source terms.  For software released under a copyleft open source license, such terms would normally be incompatible with the license.  But the licensor can permit it anyway, because as the copyright holder, they are the only ones who could conceivably sue for copyright infringement, and thus they can agree for a fee *not* to sue.  That is what is being sold on the proprietary side of a dual-licensing arrangement: permission to redistribute the software under terms that would otherwise be incompatible with its open source license.

In practice, however, a vendor that has a leadership position in a project, and is the copyright owner of the open source code, enjoys a tremendous advantage in product marketing and comparative analyses.  This is why dual-licensing works as a business method: while anyone can in theory make commercial use of the code, there is still a significant and persistent market-shaping advantage enjoyed by the primary vendor.

When implementing dual-licensing, the vendor should incorporate outside code contributions only from contributors who have signed a sufficiently strong [contributor agreement](http://wiki.civiccommons.org/Choosing_a_License) as to allow the vendor to relicense that contributor's code as the vendor wishes.  Generally the contributor agreement must be an actual copyright assignment, although there could in theory be agreements that give the vendor the necessary rights without actually transferring copyright.  Note that some contributors may [resist](http://lwn.net/Articles/359013/) signing an agreement that gives the vendor one-sided rights over the program as a whole (rights that the contributor herself doesn't have), so in some cases dual-licensing can result in fewer outside code contributions.

See also [multi-licensing](http://en.wikipedia.org/wiki/Multi-licensing).

## What about a government-specific license?

Currently, none of the commonly-accepted open source license include certain features that are typical & expected in civic procurement:

* No "law selection" clauses. Most government procurement regulations require the application of local state law or federal contracting law to the material terms and conditions of any contract (including software "right to use" licenses).
#No venue selection clauses (i.e., site and means for dispute resolution). Many state and federal procurement regulations require that disputes be resolved in particular venues.
#Rights assignment issues. Open source licenses do not have "government rights" provisions, which clarify that the software is "commercial software" and thus not subject to the draconian rules of federal procurement that may require an assignment of rights to the software when the government funds development. (There may be state equivalents; not sure.)
* Patentability issues. Although some open source licenses have (relatively weak) patent reciprocality clauses, they generally do not contain "march-in rights" or other similar provisions that may be required by (at least) federal procurement regulations for software development. This may not matter for DC per se, but it could become relevant later if, say, the project wants to accept federally funded code contributions.
#Enforceability issue. Contracting with states often requires waiver of sovereign immunity to make licenses meaningfully enforceable.

These issues are [discussed in more detail](http://www.trustthevote.org/a-license-to-adopt) at the Open Source Digital Voting Foundation. The OSDVF is in the process of creating a new open source license that resolves these issues, and they have [a draft](http://www.trustthevote.org/osdv-foundation-public-license-draft-published-for-review) up for review. However, it is not ready for real-world use as of early September 2010. Until it is ready, a reasonable solution is to release code under the open source license of your choice for now.

## Contributor License Agreements: How to Accept Code Contributions Safely

Whatever license or public domain option you choose, make sure that when accepting code contributions, you receive a signed *Contributor License Agreement* from each contributor. This will allow you and others to safely redistribute their contributions, and possibly to change to another open source license later (e.g., the upcoming OSDVF license). See [[Contributor Agreements]] for more.


Copyright - Creative Commons Attribution 3.0 Unported License
