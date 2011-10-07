=======================================
Python is Only Slow If You Use it Wrong
=======================================

Author
-------
  * Avery Pennarun (http://twitter.com/apenwarr)
  * Works at Google

Bup
----
  * Written in Python
  * Backup software
  * Uses Git as a data store
  * 80 megs/second

sshuttle
---------
  * VPN that handles wireless speeds
  * Also in Python


How to Use Python Wrong
-----------------------
  * Tight Inner Loops
  * In compiled languages, you have these often
  * Really bad in Python
  * Line of code in Python is 80-100x slower than C
  * Keep it in a higher level

Ways to Make it Fast
--------------------
  * Use Regex and C modules
     * Word based instead of char based ~5x faster
     * Will run it in C
     * Most of bup is Python, small bit in C to speed it up
  * 100% Pure is not pragmatic
  * CPython has a really good C API
     * Java doesn't, it's super painful 
  * Python + C is winning so far
     * C is for tight inner loops
     * Python for the higher level

Threads
-------
  * Computation threads are useless, because of GIL
     * Sometimes worse than single threaded
  * Okay for I/O
     * GIL will release for I/O
  * fork() works great for both 
     * Recommend to use it all the time
     * No GIL
     * Trick is getting info from process to process
     * Bup uses this
     * No weird locking interactions
  * C modules can use threads
     * Can release GIL when you get objects
     * Run threads
     * Get GIL when computations are done
     * Can get high performance
  * CPU Bound threads in Python is doing it wrong
  * Question from audience: Scipy has Weave, which will allow you to inline C code.
    * Dynamic compilation
  * There are workarounds for the GIL

Garbage Collection
------------------
  * Python is both refcounting and gc
  * Refcounting
     * Whenever you use a variable, increase reference count
     * Whenever you stop, decrease the reference count
     * Terrible, terrible thing with threads
     * Need to lock on refcounts
     * GIL solves this problem
  * Shows graphs of programs memory and time
     * Allocates 10k of space a lot
     * Refcounting sematics allow Python lower mem usage than Java
  * Testing Java
     * 3 different tests
     * Shows one where it allocates as much memory as possible
  * Sometimes Python is Garbage Collected
     * Mutual referencing objects that have ref count of one
     * Backup GC finds this, and collects them
     * Shows example on how to do this
     * Pretty complicated in order to get across the GC
     * Then it relies on sucking up tons of memory, and getting it later
     * Advice: Stay away from GC
        * Break circular references
        * Most common, trees with reference to parents
           * Full tree need to be GC'ed
        * Better: use the `weakref` module
     
     




