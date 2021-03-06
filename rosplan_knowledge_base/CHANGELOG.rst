^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package rosplan_knowledge_base
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.0.10 (2016-11-22)
-------------------
* Making the knowledge base persistent using mongodb (`#10 <https://github.com/LCAS/ROSPlan/issues/10>`_)
  * Moving main function into main.cpp
  Making functions in KnowledgeBase virtual to override
  Adding Mongodb interface class
  Adding persistent knowledge base
  Adding/querying knowledge/goals done.
  Still missing: removing knowledge.
  * most of the functionality replaced with mongo queries. Instance query still missing.
  Needs clean-up.
  * First working version of persistent knowledge base
  * Allowing to start the persistent or non persistent version based on param and cleanup of prints and unused params.
  * Making mongo-cxx-driver optional for compilation
  * Adding db params to launch files.
  * Fixing a bug where a query that would not return a result deletes the whole DB
  * Adding a clear goals service.
  * Setting the planner timeout to 1 second
  * Advertising new service
* Contributors: Christian Dondrup

0.0.9 (2016-09-14)
------------------
* Removing mongodb from launch files. (`#9 <https://github.com/LCAS/ROSPlan/issues/9>`_)
  Also commented the two lines that drop the message store in knowledge base.
* Contributors: Christian Dondrup

0.0.8 (2016-09-12)
------------------

0.0.7 (2016-09-12)
------------------

0.0.6 (2016-09-12)
------------------

0.0.5 (2016-09-09)
------------------
* Fixing duplicated parameter list in operators service (`#7 <https://github.com/LCAS/ROSPlan/issues/7>`_)
* Exposing domain_path in launch files.
* Merge branch 'master' of https://github.com/KCL-Planning/ROSPlan into merge-upstream
* Added getDomainPredicateDetails service.
  Service is used by the sample action interface to know the correct parameter labels with which to update the state.
* Added default domain file to stop KB failing.
* updated code and launch files to use "/rosplan/" as prefix of configuration parameters instead nodes names.
* removed old MongoDB directory in "knowledge_base" package, now it is stored in "rosplan_config".
* created "rosplan_config" package to store common information as MongoDB and planner binaries.
* updating squirrel branch to fix bug in turtle demo
* Updated action interface to make KB changes
* Added domain operator details service
* knowledge base to VAL; rqt dispatcher
* Revert "changed maintainer to not sending emails to the wrong people"
  This reverts commit a041b5defb4c41ac131b209a72df57ff6358f7fe.
* ROSPlan can now dispatch contingent plans.
  Observations are not checked properly.
  KnowledgeItems can now be negative
* updated query service to return bool array
* Knowledge Array and some parsing
* Contributors: Bram Ridder, Christian Dondrup, Diego Escudero, Marc Hanheide, m312z

0.0.4 (2016-04-21)
------------------

0.0.3 (2016-04-20)
------------------
* Install target and paths (`#3 <https://github.com/LCAS/ROSPlan/issues/3>`_)
  * added install targets (fixes `#2 <https://github.com/LCAS/ROSPlan/issues/2>`_)
  * made parameters private and included package path prefix for defaults
  * created absolute path for pre-compiled planner binary `popf`
* Contributors: Marc Hanheide

0.0.2 (2016-04-19)
------------------

0.0.1 (2016-04-19)
------------------
* changed maintainer to not sending emails to the wrong people
* Merge branch 'master' of https://github.com/KCL-Planning/rosplan
* clear knowledge service in knowledge base
* Added empty file for database dir
* Added flex dependency so that you can use rosdep to install the prerequisites.
* Fixed some domain parsing bugs
* Merge branch 'master' of https://github.com/m312z/ROSPlan
  Conflicts:
  rosplan_knowledge_base/include/rosplan_knowledge_base/DomainParser.h
* Domain fetching services
  Cleaner knowledge item names
  Removal of instance attributes
* Domain parsed setup
* Domain parsing in the knowledge base. New domain structure.
* Removed test robot
* Rewrite of Knowledgebase, preparing for domain parsing
* x
* Fetch all instances
* Remove goal service
* Better knowledge fetching
* Updated filter
* Fix for removal loops
* Fixed same/contains knowledge function
* Checking for preconditions updated
  Fixed bug in query knowledge service
* Now checking for preconditions during dispatch
  Added knowledge query to knowledge base
  Fixed initial values for dispatch flags
* Reading waypoints from file
* Update CMakeLists.txt
* Fixed minor misnamings in CMakeLists
* Fixed bug in domain attribute removal
* mission filter properly separated from planning filter
* Moved roadmap into own package
* Updated Planning system to use proper service names;
  Added turtebot demo
  Knowledge base now clears the scene database
* Altered Knowledge base updates to be services.
* Bug fixes in domain functions
* Updated roadmap server to use costmaps; modified launch file to match.
* Getting rid of catkin warnings. Everything so tidy.
* Continued rewrite of planning loop; planning environment fixed.
  Very minor changes elsewhere.
  Domain simplified to only movebase compatible.
* Started rewrite of planning system.
  Added timed dispatch from PANDORA.
  Added interfaces and knowledge base from SQUIRREL.
* Contributors: Marc Hanheide, Michael, Michael Cashmore, fsuarez6, m312z, michael
