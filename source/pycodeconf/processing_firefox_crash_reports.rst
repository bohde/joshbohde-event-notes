============================================
Processing Firefox Crash Reports With Python
============================================

Author
------
  * Laura Thompson (http://twitter.com/lxt)
  * Works on lots of internal tools at Mozilla

Socorro
--------
  * Named after an array in New Mexico
  * Is today's browser more or less crashy than yesterday's? 
  * If you see the Firefo crash popup, please submit it.
  
  * Shows Mozilla Crash Stats https://crash-stats.mozilla.com/products/Firefox
  

Architecture
------------
  * Collector 
     * web.py app behind apache
     * Puts on disk
  * Store in HBase (crashmover)
  * Write to Postgres by monitor
  * Webapp and API
  * All Python


Lifetime of a Crash
-------------------
  * Raw dump submitted by POST, JSON + minidump
  * Stored   
  * Processed

Processing
----------
  * Processing spins off minidumpstackwalk (msdws)
  * Tries to regenerate stack
  * Processor generates a signature
  * Tries avoid things like malloc
  * Writes to Postgres, which acts like a large, relational cache.

Backend Processing
-------------------
   * Cron
   * Calculate aggregates
      * Top crashers by signature
      * URL
      * Domain (hates Farmville)
   * Process incoming builds
   * Match known crashes to mozilla bugs
   * Dupe detection
   * Match up crash pairs, e.g. plugin containers and browsers
   * Generate CSV extracts for engineers for analysis

Middleware
----------
  * Move data access to REST API
     * Allow engineers to build apps against the data
  * Enable to rewrite app in Django in 2012
  
Webapp
-------
  * How to visualize? 
     * Many builds: release channel, nightly, hourly
  * Reporting in build time
     * Rebuilding in Django in 2012, because it's Crufty
     * Maybe Flast
  * Almost all new Mozilla apps are Django
  * Don't need models, though

Implementation
---------------
  * Use Python2.6
  * Postgres 9.1, some stored procedures
  * memcached
  * Thrift for HBase access
     * HBase written in Java
     * Thought about rewriting Hbase parts on JVM
     * Decided not to, Clojure not common, Jython for various reasons

Scaling
-------
  * Different
    * Usually scale to millions of users.
  

