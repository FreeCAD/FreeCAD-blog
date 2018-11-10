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
This should be the first place to search for awnsers if you have any questions. 

*Note:* When you create your account, it might take a while before its activated as the process is currently manual, this is to keep spam bots out.

Issues/Tickets
--------------
FreeCAD uses mantis: https://freecadweb.org/tracker/ for bug reporting and feature requests, in order to create issues you will have to create an seperate mantis account. 

As we are getting a lot of reports please follow the rules before creating a new issue

1. First post to forum to verify their issue.
2. Link said thread to ticket and vice-a-versa; 
3. Use the most updated stable or development versions of FreeCAD
4. Post your Help>About FreeCAD>Copy to clipboard version info
5. Post a Step-By-Step explanation on how to recreate the issue
6. If possible, upload an example file to demonstrate problem. 

Before you post an new issue/feature request make sure to post your bug/issues/feature requests on the forum in [this] thread.

Documentation
-------------
FreeCAD uses MediaWiki for its documentation. To be able to modify the wiki, you must request access from [here]. 
To get an Wiki account we require you to have an forum account with at least 1 post.
Before you start changing things in the wiki please read this page: https://www.freecadweb.org/wiki/WikiPages
There is a lot of rules on how to write on the wiki to keep it good, translated and up to date. Its a good idea to discuss the additions / changes you want to make in the wiki section of the forum before you follow through.
 
Code
----

The FreeCAD codebase is mostly C++ and Python, we are currently migrating to Python3, new contributions based on Python2.X is frowned upon.
The gitrepo is hosted at https://github.com/FreeCAD/FreeCAD

If you want to develop for FreeCAD you should look into creating your own workbench or modifying an existing workbench.

Given that you have the dependencies to build and run FreeCAD this is how you checkout and build the code:

git clone https://github.com/FreeCAD/FreeCAD.git freecad-code 
cd freecad-code
mkdir build
cd build
cmake .. 
make -j$(nproc)

More detailed instructions can be found [HERE]
