==========================
What Makes Python AWESOME?
==========================

Author
------

  * Raymond Hettinger (@raymondh)


Context for Success
-------------------
  
  * OS License
  * Commercial distributions
     * Sponsor advancements
  * Zen
     * Guides the language and community
  * Community
     * Killer feature
  * Repositories (Pypi)
     * Solved problems are a `pip install` away.

High level qualities
--------------------

  * Ease of learning
     * Can build a Python programmer in a week and a half
  * Rapid Dev Cycle
     * Used in a high frequency trading company
     * More important to react to market
  * Economy of Expression
  * Readability and Beauty
     * Makes it easy to work in, and less tiring
  * One way to do it
     * Once you learn an aspect, you can apply it somewhere else


A bit of Awesomeness
--------------------

  * Five minutes to write code to find duplicate files.
  * Can throw away. 
  * How long to write in C?
     * Infinite
     * You won't write it
     * Python programmers write things C programmers won't.
  * Just the same as any other scripting language?

Why is Python Awesome?
======================

Indentation
-----------
  * How we write psuedocode
  * Contributes to readability
  * Shows an example of indentation in C lying
     
Iterator protocol
-----------------
   * Lots of stuf is iterable
   * Hold the language together
   * sets, lists, dicts, files
   * shows `sorted(set('abracadabra'))`
   * `sorted(set(open(filename)))`
   * Like legos: fit together perfectly
   * Shows an analogy between that and Unix pipes.
   * Not enough, GOF pattern

List Comprehension
------------------
  * More flexibile than functional style

Generators
----------
  * Easiest way to write an iterator
  * Adds one keyword (yield)
  * Makes tricky iterators easy

Generator Expressions
---------------------
  * Produce values just-in-time
  * `sum(x**3 for x in xrange(1000000))`
  * In Pypy, roughly C speed
  * setcomps and dictcomps

Generators that accept Input
----------------------------
  * generators support send(), throw(), and close()
  * Unique to Python
  * Can make Twisted's inline deferreds using this
  * A state machine with callbacks. 
  * Write code that looks procedural, but uses callbacks
  * Monocle (https://github.com/saucelabs/monocle), Twisted inline deferred
  * Fantastic improvement of callback code.

Decorators
----------
  * Expressive
  * Always worked for function
  * Initial response: Syntactic sugar
  * Community rose up and demanded it from Guido.
  * Easy on the eyes
  * Shows example using itty (https://github.com/toastdriven/itty) using decorators for routing.
  * Ping into another machine using curl to lookup environment variables in 3 lines.
  * Web service in 20 lines, made possible by decorators
  * Thanks Django!

With Statement
--------------
  * Clean, elegant
  * Profoundly important
  * Sandwich analogy
  * Subroutines factor out the 'meat' of the code
  * With statments factor out the 'bread' of the code
  * Factors out common setup and teardown methods.
  
Abstract Base Classes
---------------------
  * Uniform definition of what it means to be a sequence, mapping, etc.
  * Ability to override `isinstance()` and `issubclass()`
  * Duck-typing says: "If it says it's a duck..."
  * Mixin capability (DictMixin)
  * Can provide the base of a class 
     * shows using a list-based set with `__iter__`, `__contains__`, and something else
     * Mixin provides the rest

