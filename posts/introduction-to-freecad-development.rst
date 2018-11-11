.. title: Introduction to FreeCAD development
.. slug: introduction-to-freecad-development
.. date: 2018-11-10 21:11:10 UTC
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text

This is the first post in a series that aims to give you a basic understanding of how development for FreeCAD is done and how you can contribute.

Forum
-----
The FreeCAD forum: https://forum.freecadweb.org/ is the primary place for communication between FreeCAD users as well as developers.
This should be the first place to search for answers if you have any questions.

**Note:** When you create a forum account, it might take a while before it's activated as the process is currently manual. This is done to limit spamming.

Issues/Tickets
--------------
| FreeCAD uses `MantisBT <https://mantisbt.org/>`_ as its tracker for bug reporting and feature requests.
| The FreeCAD tracker address is https://freecadweb.org/tracker/
| **Note:** In order to create issues you will have to create an separate MantisBT account.

As we are getting a lot of reports please follow the rules before creating a new issue

1. Make sure you're using the most updated stable or development versions of FreeCAD.
2. **PLEASE PLEASE PLEASE** post to FreeCAD forum to verify the issue.
3. Only after community vetting, open a ticket and link said thread to ticket and vice-a-versa.
4. Post your **Help>About FreeCAD>Copy to clipboard** version info in to forum thread and ticket.
5. Post a Step-By-Step explanation on how to recreate the issue.
6. If possible, upload an example file to demonstrate problem.
7. If there is a crash involved, please consider `Debugging <https://freecadweb.org/wiki/Debugging>`_ and attaching the traceback to the ticket.

Documentation
-------------
| FreeCAD uses `MediaWiki <https://mediawiki.org>`_ for its documentation. To be able to modify the wiki, you must `request access from the FreeCAD wiki admins <https://forum.freecadweb.org/viewtopic.php?f=21&t=6830>`_.
| **Note:** To get an Wiki account we require you to have a forum account with at least 1 post.
| Before you start changing things in the wiki please read the `WikiPages <https://www.freecadweb.org/wiki/WikiPages>`_ guidelines,
| There are several rules on how to write on the wiki to keep it organized, high quality, translated and up to date. It's our practice to discuss the additions/changes one wants to make in the `FC wiki subforum <https://forum.freecadweb.org/viewforum.php?f=21>`_ prior to posting.

Code
----
The FreeCAD codebase is mostly C++ and Python, we are currently migrating to Python3, new contributions based on Python2.X are frowned upon.
The git repo is hosted at https://github.com/FreeCAD/FreeCAD

Development
-----------
If you're interested developing for FreeCAD please look into::

1. creating your own workbench (See footnote[#f1]_ footnote[#f2]_  footnote[#f3]_)
2. modifying an existing workbench (View source code of any external workbench at `FreeCAD-Addons Repo <https://github.com/FreeCAD/FreeCAD-addons>`_)
3. creating your own macro (Read more about `FreeCAD Macros <https://www.freecadweb.org/wiki/Macros>`_ & the `FreeCAD Macros Repo <https://github.com/FreeCAD/FreeCAD-macros>`_ )

Given that you have the dependencies to build and run FreeCAD this is how you checkout and build the code::

  $ git clone https://github.com/FreeCAD/FreeCAD.git freecad-code
  $ cd freecad-code
  $ mkdir build
  $ cd build
  $ cmake ..
  $ make -j$(nproc)

More detailed instructions can be found [HERE]

Footnotes
---------
.. [#f1] https://www.freecadweb.org/wiki/Workbench_creation)
.. [#f2] https://www.freecadweb.org/wiki/Module_Creation)
.. [#f3] https://github.com/FreeCAD/Workbench-Starterkit)
