BrowserQuest
============

BrowserQuest is a HTML5/JavaScript multiplayer game experiment.


Documentation
-------------

Documentation is located in client and server directories.


Instructions
------------

These were tested with node v0.6.3 and browserquest git hash/version
of eb63d58fc.

Use your favorite editor to copy/edit config files in the
server subdirectory.  For example...

    $ cat config_local.json
    {
        "port": 9000,
        "debug_level": "debug",
        "nb_players_per_world": 200,
        "nb_worlds": 5,
        "map_filepath": "./server/maps/world_server.json",
        "metrics_enabled": false,
        "memcached_host": "10.3.121.192",
        "memcached_port": 11211,
        "event_db_module": "memcache",
        "event_db_host": "10.3.121.192",
        "event_db_port": 11211
    }

Grab the right npm modules, using...

    $ npm install -d

For example...

    $ npm install -d
    npm info it worked if it ends with ok
    npm info using npm@1.1.0-alpha-2
    npm info using node@v0.6.3
    npm info preinstall BrowserQuest@0.0.1
    npm WARN websocket-server@1.4.04 package.json: bugs['web'] should probably be bugs['url']
    npm info build /Users/steveyen/work/membase/dev/scratch/cbquest
    npm info linkStuff BrowserQuest@0.0.1
    npm info build /Users/steveyen/work/membase/dev/scratch/cbquest/node_modules/http-server
    npm info preinstall http-server@0.5.1
    npm info linkStuff http-server@0.5.1
    npm WARN prefer global http-server@0.5.1 should be installed with -g
    npm info install http-server@0.5.1
    npm info postinstall http-server@0.5.1
    npm info install BrowserQuest@0.0.1
    npm info postinstall BrowserQuest@0.0.1
    
    npm info ok

To start the websocket server...

    $ node server/js/main.js

To install the webserver...

    $ cd client
    $ ln -s ../shared
    $ npm install http-server

Use your favorite editor to copy/edit config files in the
client/config subdirectory.  For example...

    $ more config/config_build.json
    {
        "host": "10.17.28.124",
        "port": 9000
    }

To launch the webserver...

    $ cd client
    $ http-server -p 9010

Next, browse to http://127.0.0.1:9010 and start playing.

Hints on webserver...

Perhaps also try...

    $ cd client
    $ npm install -g http-server


License
-------

Code is licensed under MPL 2.0. Content is licensed under CC-BY-SA 3.0.
See the LICENSE file for details.


Credits
-------
Created by [Little Workshop](http://www.littleworkshop.fr):

* Franck Lecollinet - [@whatthefranck](http://twitter.com/whatthefranck)
* Guillaume Lecollinet - [@glecollinet](http://twitter.com/glecollinet)