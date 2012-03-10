===============
Advanced Celery
===============

Author
------
  * Ask Solem
  * Work at VMware, on RabbitMQ team

Overview
--------
  * Flexible and Reliable message queue system
  * Granularity: the less computation, the more fine grained the task is
    * Can reuse connections, etc
  * Chunking
    * Grouping fine-grained tasks to reuse resources

Chords
------
  * Sync primitive
  * Known as a barier
  * Callback the body with the results of the headers
  * Native support in Redis, with good enough fallbacks for others
  * demo of parallel summariazation using chords
  * Can use this to implement MapReduce
  
Blocking
--------
  * Is bad
  * Timeouts

Routing
-------
  * Smart routing
  * CPU based routers would be nice

Cyme
----
  * https://github.com/celery/cyme
  * A distributed Celery instance manager
  * HTTP based API
  
