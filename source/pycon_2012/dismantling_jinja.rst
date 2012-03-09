======================================================
Code Generation in Python: Dismantling Jinja
======================================================

Author
------
  * Armin Ronacher

Why?
----
  * Isn't it evil? 
  * A security problem?
  * Bad for performance?
  * Not if you do it right. 
  
Security
--------
  * Code Injection
  * Pollute namespace
     * Change local variables
     * Can evaluate code in different namespace

Performance
-----------
  * Alternative: Write an interpreter
  * Too slow
  * Not suitable

Eval 101
--------
  * Compile function to make code objects
  * evan can work on a namespace
  * Using ast module, can alter underlying structure
  * Can use ast to add in line numbers to nodes
  * Don't pass strings to eval/exec, but use code objects
  * Explicit compliation and namespaces, to fix problems

Jinja
-----
  * Jinja and Django have C inspired scoping rules
  * Pipeline
     * Lexer
     * Parser
     * Identifier analyzer
     * Code generator
     * Python source
     * Bytecode
     * Runtime
  * Only runtime is necessary
  
Scoping
------
  * Context objects are dict-alike
  * Slow
  * Resolve in context ahead of time  
 
Code Generation
---------------
  * Low level
  * Target byte-code
  * High level
  * AST generation
  
  * Bytecode doesn't work on appengine, and is implementation specific
  * Would be nice to map jinja to bytecode
  
  * Ast is limited, easier to debug, and doesn't segfault

Tale of Two Pieces of Code
--------------------------
  * scope in a function is faster than global scope
  * lookup via index instead of name
  * local dictionary isn't generally used
  * semantics can be mapped to fast execution environment
  * Jinja context is data source
  * Django context is data store
  * You cannot modify context in Jinja

jsonjinja
---------
  * Semantics of jinja, in javascript
  * https://github.com/mitsuhiko/jsonjinja



