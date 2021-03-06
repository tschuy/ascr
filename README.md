ascr
====

A simple screenshot uploader to upload screenshots instantly to a remote
webserver. Written because it shouldn't be more convenient to upload to imgur than
a remote SSH host.

Usage
-----

``ascr``: the main executable. Just run on its own it will use import to
take a screenshot and upload it with the date/time as the filename.

If you have xclip installed, it will print the URL on screen and copy it to
your clipboard. Otherwise, it will just print it to the screen.

``ascr filename`` or ``ascr filename.png``: give the screenshot a specific
filename.

``ascr -w`` takes a screenshot of a single window. This feature has only been
tested on Linux, and will not work with OS X (pending your pull request!). It
works with ``-i`` and the filename options.

Alternatively, to upload to Imgur, just run ``ascr -i``. The URL will be copied
to your clipboard and displayed just like it is for an SSH uploaded image.

Configuration
-------------

``ascr`` uses either an ``.ascrrc`` file located in your home directory or an
``ascr.conf`` located in ``~/.config/`` for configuration. An example file with
the three mandatory options has been provided:

    SERVER=tschuy@ash.osuosl.org
    DIRECTORY=~/public_html/screenshots/
    URL=https://ash.osuosl.org/~tschuy/screenshots
