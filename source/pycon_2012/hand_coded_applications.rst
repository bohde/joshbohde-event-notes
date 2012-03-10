=====================================
Hand Coded Applications with SQLAlchemy
=====================================

Author
------
  * Michael Bayer

What's a Database
-----------------
  * We can put data in and get it out
  * Can do queries that allow us to find records with attributes

Relational Database
-------------------
  * Can create derived tables with suqueries
  * Set operations
  * ACID

How Talk to DB
---------------
  * DBAPI
  * Abstraction layers

ORM
---
  * Maps to relations
  * Can map to multiple relations
  * Can map object heirarchies to tables
  * How abstract should these be?
    * Should document stores work? 
  * Relational features are under/misused which causes the mismatch
  * Best to not hide, but to automate
  * Explicit decisions and automation is "hand-coded"

Hand-Coded
----------
  * Make decisions about everything
  * Automate these decisions for ease
  * Opposite of "wizards", "plugins", and APIs that make implementation decisions
  * Can still use libraries and frameworks

Polymorphic Association
-----------------------
  * Map multiple classes to something using GenericReferences
  * Does magic for us
  * Sometimes called GenericForeignKey
  * This breaks the C in ACID
    * Can generate FK that doesn't point to anything
  * Implicit design decisions
    * Magic tables
    * source code stored as data, which is coupling
    * Application layer responsible for consistency

SQLAlchemy's Response
----------------------
  * Declarative Base
    * Composable patterns
  * HasOwner, and PortfolioAssets defaults
  * Define convention for polymorphic association
