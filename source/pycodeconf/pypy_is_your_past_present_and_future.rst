======================================
PyPy is your Past, Present, and Future
======================================

Author
------
  * Alex Gaynor (http://twitter.com/alex_gaynor)
  * Still in school, core Django, CPython, and Pypy committer

Intro
------
  * There are 2 things faster than C
     * Neutrinos
     * Pypy

Story
-----
  * Armin wanted to write a JIT for Python (Psyco)        
  * Psyco was the written by Armin. 
  * Kind of messing.
  * Generators came along, and not supported
  * 64-bit computers weren't supported either
  * Started writing Python in Python
  * About 2000x slower than CPython  
  * Somethings in the standard library were in python
  * Copied some optimizations over (TimSort)
  * Writing JITs sucked.
  * Writing a JIT generator for arbitrary languages is much simpler than writing a JIT for Python
  * ~2-3 years ago Alex got into Pypy
  * Beat C in str_cmp ~1 month ago
  * http://speed.pypy.org
  * Tries to show example of real time video analysis, mplayer broke.


Numpy
------
  * Science likes big datasets, use Numpy
  * Numpy is in C
  * Numpy likes speed, so does pypy
  * Started reimplementing Numpy in Pypy
  
Hotspot Detection
-----------------
  * Humans are bad at detecting slow downs
  * Pypy has a JITViewer
     * http://morepypy.blogspot.com/2011/08/visualization-of-jitted-code.html
     * Allows you to view code in levels
     * Python, Assembler, etc.
  * Shows demo fo JITViewer
  * Look into code
     * "I think that's too many instructions"
     * Optimize code!
  * Shows example of `sum(x**3 for x in xrange(10000))`
  * JVM Community has good tooling
  * Python could use that too.


Current
--------
  * Usually benchmark against C
  * Experimenting with using C extensions.

Where we're going
-----------------
  * Many projects are being migrated
     * Django
  * Porting to Python3

Architecture
------------
  * Because they use a JIT Generator, can improve constantly
  * Speedups in Python3 will improve Python2

GIL
---
  * Wrote a blogpost on STM (Software Transactional Memory).
     * http://morepypy.blogspot.com/2011/08/we-need-software-transactional-memory.html

  * Think STM would be slower for single core
  * STM for multicore workloads
  * GIL for single core.
