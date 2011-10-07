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
    
