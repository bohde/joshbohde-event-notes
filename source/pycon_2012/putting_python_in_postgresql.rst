======================================================
Putting Python in PostgreSQL
======================================================

Author
------
  * Frank Wiles

Why
---
  * Usually you want pl/pgsql
  * Sometimes you want a scripting, with libraries, etc.

Installing
----------
  * Aptitude: `postgresql-plpython`
  * homebrew

Setting up the database
-----------------------
  * createlang plpythonu <databasename>
  * Check with `SELECT * FROM pg_language`
  * Python is untrusted
  * Can set this up in templates

Writing your first function
---------------------------
  * CREATE OR REPLACE FUNCTION
  
Debugging
---------
  * plpy.notice, debug, error, and fatal
  * Will access the log file directly
  * Can use logging
  
Problems
---------
  * Pain to maintain and debug
  * Can confuse the dba
  * Not free, cached

When
----
  * Rolling up/aggregating data
    * Remove network, sql parsing to keep runtime low
  * Enforce new constraints that aren't in SQL
  * Protect data integrity

Triggers
--------
  * CREATE TRIGGER...
  * Throw a Python exception
  * The TD variable has a lot of stuff in it

Redis
-----
  * Can use system libraries
  * Update Redis unread count automatically

What can you do?
----------------
  * Executing other sql, create materialized views
  * plpy namespace has execute

Ideas
-----
  * Lots of them
  * Celery tasks, caches, backups, apis, zeromq
  * Emails, inserts into another system, send an sms
  
Q&A
---
  * Limit the runtime of the procedure?
    * Don't think so
  * Test Python Code?
    * Fake it outside
  * Automatically cache?
    * Have to say it's immutable
  * How easy is it to specify a python binary?
    * Can specify per Postgres cluster
  * Run postgres queries inside query, infinite loop? 
    * Will time out eventually? 
    * Not yet, will be in 9.2
  * Interpreter external or internal?
    * Didn't hear
  * Timeout kill trigger?
    * Could have connection timeout in code
  * PGSQL v. Python was a magnitude difference
    * Not surprisingly
  * Pypy or Jython?
    * Probably not
    * Not yet
  * Table functions? 
    * Haven't done much with that, mostly just materialized views

  
