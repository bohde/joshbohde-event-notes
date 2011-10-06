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

        
  
