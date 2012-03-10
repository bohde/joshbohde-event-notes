=====================================
Flexing SQLAlchemy's Relational Power
=====================================

Author
------
  * Brandon Rhodes

Denormalization
---------------
  * Quick to render, hard to update
    * e.g. IMDB updating an actor where it's stored with movies
 
Normalization
-------------
  * Only store data once
  * Easier update
  * Need to pull data from multiple places

SQL
----
  * Need to model relationships through intermediary table
  * No composite data types
     * If you see fields like actor_1, actor_2, etc. something is wrong

Storage is Slow
---------------
  * Indexes let us jump to right part faster
  * Keeping records sorted on disk is slow
  * Indexes make this faster

How to make it fast?
--------------------
  * Ask one question
  * Use explain and indexes 
  * Domain knowledge can tell us how we can optimize a query
    * Postgres has an analyzer that does this well

The O Error
-----------
  * misconception: An ORM just deals with objects, and hides the relational
  * You need to know relational





