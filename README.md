prerender-memjs-cache
=======================

Fork of prerender plugin for memjs caching by [lammertv](https://github.com/lammertw/prerender-memjs-cache), to be used with the prerender node application from https://github.com/prerender/prerender.

How it works
------------

As original plugin, this fork will store all prerendered pages into a memcache service using  [memjs client](https://github.com/alevy/memjs). But this fork also extends the original plugin with expiration functionality.


How to use
----------

In your local prerender project run:

    $ npm install hooke/prerender-memjs-cache --save

Then in the server.js that initializes the prerender:

    server.use(require('prerender-memjs-cache'));

Set the page's time-to-live value in your environment:

    export PAGE_TTL=3600


Configuration
-------------

The plugin uses the memjs module. It's configuration is explained at https://github.com/alevy/memjs/blob/master/README.md.

TODO
-----

possibility to set page TTL on each caching operation
