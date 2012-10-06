icecast2-munin
==============

Requirements
------------
 * Munin
 * Python 3.2 or above
 * [Requests python library](http://docs.python-requests.org/en/latest/ "Requests")
 * An icecast2 server

What?
-----
This is a plugin for munin to record global listener figures, mountpoint total, and individual mountpoint listener figures for your icecast server.

Remarks
-------
This plugin is based off a icecast2 plugin which was found in the munin plugin repository. It had no author, no licence, was using and old version of python and didn't work out of the box. I would credit you, but I don't know who you are, so hello.

I'm using the requests python library, because urllib was being a pain with authentication, and requests is so much nicer to use. It's fairly easy to get requests installed if you use pip.