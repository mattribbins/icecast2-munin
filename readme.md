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

How to use
----------
 1. Copy icecast2_all to plugins directory (/usr/share/munin/plugins/ or /usr/lib/munin/plugins/)
 2. Set executable flag on file ($ chmod +x /usr/lib/munin/plugins/icecast2_all)
 3. Edit munin-node environment configuration ice2{host, user, pass}
 3.5. Else, edit icecast2_all configuration (host, username, password)
 4. Symlink to munin live plugins folder ($ ln -s /usr/share/munin/plugins/icecast2_all /etc/munin/plugins/icecast2_all)
 5. Restart munin-node ($ /etc/rc.d/munin-node restart)
 6. Graphs should start to appear.
 
Help!
-----
If you're stuck getting this working or notice something drastically wrong, you're welcome to email me. matt@mattyribbo.co.uk

Remarks
-------
This plugin is based off a icecast2 plugin which was found in the munin plugin repository. It had no author, no licence, was using and old version of python and didn't work out of the box. I would credit you, but I don't know who you are, so hello.

I'm using the requests python library, because urllib was being a pain with authentication, and requests is so much nicer to use. It's fairly easy to get requests installed if you use pip.