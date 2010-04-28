Muck - quick-and-dirty file-based weblog software
=================================================

The Problem
-----------

Most weblog software seems to have at least one or more of the following issues:

*   Massive amounts of resources used to "generate" content ... with very little efficency
*   Minimal capabilities to handle anything other than a single, reverse-chronological-order, list of entries 
*   A large, rabid fan base ... of people looking to exploit security holes in the software
*   Clumsy or bolted on solutions to handle attached files or metadata

Proposed Solution
-----------------

All of that aside, this is mostly just academic puttering around.  Basically I want to create something that:

+   Uses flat-files to store data (meta and non) to be used in rendering a page
+   Uses the structure of the file system wherever possible (grouping of entries in feeds, timestamps, etc)
+   (Probably) Uses Twitter as the method of commenting on a given entry
+   (Probably) Builds output to a "staging" area so that it can be rsync'd to any desired destination

Why does it look so weird?
--------------------------

So, another thing I'm trying out is just how far to take code sanitization efforts.  Everything committed will:

*   Be run through Perltidy (with Perl Best Practices settings)
*   Have "use strict" and "use warnings" turned on (with no exceptions)
*   And, just to see how weird things would get, Perlcritc turned up all the way to severity=1 (default PBP ruleset to begin with, we'll see what else to add later.) 
