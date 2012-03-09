======================================================
Stop Writing Classes
======================================================

Author
------
  * Jack Diederich

When Should I refactor
----------------------
  * When there are two methods, and one is __init__
  * When you write functions around classes
  
Evolution of an API
-------------------
  * MuffinHash replaces a dict
  * Was two lines, and obfuscated the code
  * 1 package, 20 modules

Version II
-----------
  * Easy to read
  * Two methods, __init__ and call
  
Version III
-----------
  * stdlib parts, 6 lines
  * 1 function

Namespaces
----------
  * Preven collisions
  * Not taxonomies
  * Otherwise extra things to type, remember
  * Anytime you make a class, ask "What am I using it for?"
  * Reuse stdlib exceptions
  * Don't complicate the names of your exceptions

stdlib
------
  * 200k sloc
  * avg 10 files per package
  * 165 exceptions

Classes
-------
  * great for containers
  * heapq doesn't use a class
  * Probably should be a class, since functions looke like methods
    * first param is data


