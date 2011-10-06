==============================================
The State of Packaging & Dependency Management
==============================================

Author
-----
Craig Kerstiens (http://twitter.com/craigkerstiens)
Works at Heroku

Packaging
---------
  * Need to release it

Where To Release
================

Your Server
-----------
  * Full flexibility
  * People rely on you being up
  * Breaks deploys
  * Don't do this, unless you want to provide better uptime than PyPI

Github
------
  * Awesome for dev
  * Not for release
  * Not mean to packages, but source code

PyPI
----
  * Please release it here
  * Complain about it being down
  * 5 mirrors that are well updated
  
Managing Dependencies
---------------------
  * Use pip
     * Supports uninstalling
     * Lots of small improvements
     * Supports version control 
     * Don't use this in production
  * Use virtualenv
     * Great for sandboxing
     * Destroy and recreate it often
     * Pin your dependencies

Pinning
-------
  * Only deploy specific versions
  * `pip freeze > requirements.txt`
  * It's explicit (see the Zen)

Version Control
---------------
  * Having a github/bitbucket source is good for dev...
  * Not for prod.
  * Put tarballs on internal servers.
     
PyPI is Down
------------oG
  * `pip install --use-mirrors`, problem solved


Whats Missing
-------------
  * Not as good as Bundler from Ruby community  
  * Pip upgrade needs to be better

Recap
-----
  * Use PyPI
  * Explicit versions
  * Use mirrors
  * Need to use the tools more effectively

Questions
---------
  * A frozen requirement may have unfrozen dependencies
  * May need to tweak requirements.txt 
