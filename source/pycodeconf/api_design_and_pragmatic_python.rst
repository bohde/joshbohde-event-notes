===============================
Python For Humans
===============================

Author
------
  * Kenneth Reitz (http://twitter.com/Kennethreitz)
  * Works for Readability
  * Works on the Github Reflog
  * Used to be part of the Changelog    
  * Authored Requests, Tablib, Legit, OSX-GCC_installer, Clint, Evnoy, Httpbin
  * Makes software for humans

Talk Slides
-----------
  * https://github.com/kennethreitz/python-for-humans
  
Philosphy
---------
  * What people like about Python
     * Simplicity
     * Speed to develop
     * Pypy
  * `import this`
  * The Zen of Python, our manifesto
  * Beautiful is better than ugly
     * Syntax
  * Explicit is better than implicit
     * Compared to Ruby
  * If the implemenatation is hard to explain, it's a bad idea
     * Unless you're pypy

  * This talk will focus on there should only be one obvious way to do it.

Messing Around
--------------
  * Using Github API
  * Show's Ruby code, not beautiful but straightforward
  * When trying it in Python we get confused about what library to use
     * Python 3 helps this naming issue
  * Shows code using `urllib2`
     * Too many actions to just use basic auth
     * And there's more!
     * Github API uses 404 instead of 401, need to write our own BasicAuthHandler
     * Need to force it to send basic auth, took 3 hours
  * This would prevent people from using Python.
  
Problems
--------
  * Unclear on what module to use
  * "HTTP should be simple as the print statement"

Solution
--------
  * We need pragmatic, elegant tools.

HTTP
----
  * Has methods
  * Very simple
  * Urrllib2 is very complex, and therefore toxic

Requests
--------
  * For humans
  * Simple solution for a simple problem

Litmus Test
-----------
  * You should not have to refer to the docs everytime you want to do something simple
  * API is the most important thing
  * Handle the 95% case elegantly

Building
--------
  * Requests was very simple at first, but it resonated with people
  * Grew to handle more stuff
  * 17th most watched project on Github

Subprocesses
------------
  * Powerful, effective, second worst API
  * Docs lacking
  * Follows C API
  * Mostly docs that are lacking

Proposed Solution
-----------------
  * Envoy
  * Mostly the same API as Requests
  * Pipe, read stdout, etc.
  * Get it done quickly and effectively

File and System Ops
-------------------
  * Surveyed dev ops
  * Shutil, sys, etc. are confusing
  * Limits adoption by dev ops guys

Install Python
--------------
  * Surveying room on installation methods on OSX
  * Many chosen
  * "What happened to one obvious way to do it?"

XML
-------------
  * `etree` is terrible
  * `lxml` is awesome
  * We need to adopt a better standard
 
Packaging and Dependencies
--------------------------
  * `pip` or `easy_install`
  * `setuptools`?
  * `Distribute`
     * How is it better than setuptools?
  * We need simple instructions on how to install, and release packages

Dates
-----
  * Some good 3rd parties
  * Stdlib not good enough

Unicode
-------
  * It's a simple problem
     * Room erupts in "No it's not!"
  * Should be easy

Testing
-------
  * Unittests
  * Didn't get the downside

Installing Dependencies
-----------------------
  * Asked room about difficulties
  * Almost everyone had difficulties

Hitchiker's Guide to Python
---------------------------
  * http://python-guide.org
  * Teach the best practices
  * "There should be one-- and preferably only one --obvious way to do it"
  * Brief overview


