=================
Embracing The GIL
=================

Author
-------
  * David Beazley (@dabeaz)

Intro
-----

  * Railed on GIL at PyCon, thought it deserved some Love
  * Godwin's Law of Python

Interest
--------

  * Fun hard systems problem
  * Likes to break GILs as a hobby

Threads are Useful
------------------

  * People love to hate on threads...
  * Because they are being used. 
  * They solve tricky problems.

In A Nutshell
-------------

  * Python code -> VM instructions
  * Can't execute VM instructions concurrently, therefore locking 
  * Keep things safe
    * Ref counts
    * Mutable types
    * Internal bookkepping
    * Thread safety
  * All low level.

An Experiment in Messaging
--------------------------

  * Comes up in a lot of contexts
  * Involves IO
  * Foundation for working around the GIL
  * Shows an experiment in messaging using 5 implementations
     * C + ZeroMQ
     * Python + ZeroMQ (C extensions)
     * Python + multiprocessing
     * Python + blocking sockets
     * Python + nonblocking sockets
  * Tested on xlarge EC2 instance.

Scenario 1
----------

    * Unloaded server
    * Expect ~10 seconds (10 seconds of sleep in there)
    * All roughly the same (~13 seconds for each)
    * Shows a real time example

Scenario 2
----------

    * Implement a thread to calculate Fib(200) (Referencing Node.js is a cancer)
    * C version is barely affected. 
    * Python blocking goes to 142 seconds. 
    * Real time example takes a long time.
    
Commentary
----------

    * This aggression will not stand.       


Thoughts
--------

  * Try Pypy
     * Test on Pypy (6k seconds)
     * fixed in trunk
  * Try 2.7
     * Within 2x

GUI
---

  * Uses Idle with threads (esp CPU bound)
  * Kills performance to the point of completely unusable
  * Can barely type into Idle

Thread Switching
----------------

  * GIL aquisition based on timeout
  * Thread that want the GIL must wait 5ms
  * Causes a problem on release
  * 5ms delays build up

What's Really Happening
-----------------------

  * Before send and recv, acquire GIL
  * After release

How to Fix
-----------

  * Thread priorities
  * Was in the original "New GIL" patch
  * Should be revisited

Experiment
----------

  * Has an experimental python 3.2 with priorities
  * Really minimal
  * Threads can set their priority
  * Performance that is comparable to version without threads.
  * Makes GUI completely usable.
  * Tried with 1.4k threads.

