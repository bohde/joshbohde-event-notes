=========================================
Backbone.js and Django for a Faster WebUI
=========================================

Author
-------

  * Leah Culver (http://twitter.com/leahculver)
  * Cofounder of Pownce, one of the first big Django applications.
  * Works at Convore (https://convore.com/)

Leafy Chat
----------
  * Web frontend for IRC
  * Done in Django Dash (2008?)
  
Grove
-----
  * New project
  * Internal IRC for your company
  * https://grove.io

Chat Systems
------------
  * Built a lot of them
  * Leafy chat - only used jQuery, lots of javascript
  * Using Backbone in Grove

Examples
--------
  * Show an example of using jQuery to build UI.
  * Embedded HTML in javascript.

Backbone and Grove
------------------
  * The UI looks the same
  * Backbone gives MVC style, in a single file.
  * You can roll it yourself, making it easy to get started. 
  * Not actually MVC, actually Models, Templates, and Views
  
Models
------
  * Shows `Backbone.Model.extend({})` 
  * http://documentcloud.github.com/backbone/#Model

Collections
-----------
  * Shows `Backbone.Collection.extend({})`
  * http://documentcloud.github.com/backbone/#Collection

Views
-----
  * Highlight the Backbone Views on the Grove app page. 
  * Demonstrates Backbone Event binding
     * Creates the view from the model data
     * Bind updating view when the model changes

Templates
---------
  * Uses handlebars.js (http://www.handlebarsjs.com/)
  * Looks like Django
  * Specify templates to a view.
  * use include_raw templatetag http://djangosnippets.org/snippets/1684/

Additional Goodies
==================

Sync
----
  * Used to synchronize data on Django server
  * Shows `request.raw_post_data` to get JSON objects.
  * https://gist.github.com/1265346

Events
------
  * Can update multiple views for a single model.
