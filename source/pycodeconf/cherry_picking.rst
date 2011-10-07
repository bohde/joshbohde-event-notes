===============================
Cherry-picking for Huge Success
===============================

Author
------
  * Armin Ronacher (http://twitter.com/mitsuhiko)
  * Part of the Pocoo Team
  * Notable work: Flask, Jinja2, Werkzueg

Preface
-------
  * Framework/Language fights are boring. Just use the best tool for the job.

Twitter
-------
  * 2006: Rails, XML API
  * Now: JS Frontend, Erlang/Java
  
Does Ruby Suck?
---------------
  * No, and neither does Python
  * Both are great for prototyping
  * Application changes over time
  * Will rewrite

Solution
--------
  * Build small applications
  * Combine into a larger one
  * Builds foundation to experiment
    * Move dbs, etc.
  * Crossing language boundaries
     * Rewrite
     * Use a different library
     * Implement a service

Agnostic Code
-------------
  * Example of depending on Django too much
  * Instead of importing from Django, pass it in
     * Class instance, parameter
     * Make it specific, but not more

Example
-------
  * Drop down to WSGI
  * Usually too specific, if you only need just the url

Protocol Example
----------------
   * Compared to Python iterables
   * Flask views return wsgi apps
   * Can dispatch to a Django application, for example

Difflib
-------
   * Compares any iterable that is hashable and comparable
   * Overly specific would be strings, though that's the main use case
   * Real world use to diff HTML docs
   * Plugin Genshi to difflib to accomplish this

Interface Examples
------------------
  * Serializers
     * Missed examples

Mergepoint
----------
  * To build apps we need merge points for smaller apps

WSGI
----
  * Used with most Python web frameworks
  * Often not enough
  * Provides a framework independent environment
  * Middleware can be useful mergepoints, though overused
  * Cannot consume form data in WSGI, inject uniform html, etc.
  * Libraries that help with this
     * Werkzeug
     * WebOb
     * Paste
  * Can write short helpers to dispatch from e.g. Django to WSGI

HTTP
----
  * Language independent
  * Cacheable
  * Harder to work with, complex
  * Can do proxying, nginx
  * Caching layers for scalability
  * Problem: Need to keep them running
  * Language independent library 
  * cUrl

ZeroMQ
------
  * More modern TCP Socket
  * Language independent
  * Different topologies
     * push/pull
     * pub/sub

