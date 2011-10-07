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
