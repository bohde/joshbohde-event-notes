===================
Why PyPy By Example
===================

Authors
-------
  * Maciej Fijalkowski
  * Alex Gaynor
  * Armin Rigo

What is PyPy
-------------
  * Can't convince that they are not crazy
  * Python in Python
  * No longer speed of interpreter, speed of running program
  * Measuring memory is important

Edge Detection
--------------
  * Use dynamic objects with __get__ overridden to act like a list
  * Do edge detection on a web cam in real time
  * Implemented in Python
  * In cPython, ~7 seconds per frame

Tracebin
--------
  * Successor to JITViewer
  * Expose performance information without understanding how PyPy works

Numpy
-----
  * Believe easier to add numpy to JIT than a JIT to numpy
  * Some good initial results, but not complete

Garbage Collection
------------------
  * Don't have to call `free`
  * History of talk for Pascal
  * Everywhere now

Transactional Memory
--------------------
  * How do we use multiple cores?
    * Semaphores, events, etc.
  * Multicore usage
  * Two times the execution time
    * Where we were with GC years ago
  * Hard work

Sprints
-------
  * Come sprint on PyPy
  * We'll help with getting projects working on PyPy


