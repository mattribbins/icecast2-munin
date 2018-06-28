icecast2-munin
==============

Requirements
------------
 * Munin
 * Python 3.2 or above
 * [Requests python library](http://docs.python-requests.org/en/latest/ "Requests")
 * An Icecast2 server

What?
-----
This is a plugin for munin to record global listener figures, mountpoint total, and individual mountpoint listener figures for your Icecast servers.

Features
--------
* Generate graphs from one or multiple Icecast servers, standalone or relays.
* Filter sources listed by using Regex filters.


How to use
----------
 1. Copy icecast2_all to plugins directory (/usr/share/munin/plugins/ or /usr/lib/munin/plugins/)
 2. Set executable flag on file ($ chmod +x /usr/lib/munin/plugins/icecast2_all)
 3. Edit munin-node environment configuration ice2{host, user, pass}
 3.5. Else, edit icecast2_all configuration (host, username, password)
 4. Symlink to the munin live plugins folder ($ ln -s /usr/share/munin/plugins/icecast2_all /etc/munin/plugins/icecast2_all)
 5. Graphs should start to appear.

Help!
-----
If you're stuck getting this working or notice something drastically wrong, raise an issue on GitHub or email matt@mattyribbo.co.uk.

Remarks
-------
This plugin is based off an old icecast2 plugin from years ago which was found in the munin plugin repository. It had no author, no licence, used an old version of python and didn't work out of the box. I would credit you, but I don't know who you are, so hello!

The requests python library is used instead of native urllib which was a pain with http authentication. It's fairly easy to get requests installed by using pip.
