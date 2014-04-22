
#Introduction

ComicStreamer is a media server app for sharing a library of comic files via a simple REST API to client applications.  It allows for searching for comics based on a rich set of metadata including fields like series name, title, publisher, story arcs, characters, and creator credits.

A web interface is also available for searching and viewing comics files.

It's best used on libraries that have been tagged internally with tools like ComicTagger (http://code.google.com/p/comictagger/) or ComicRack (http://comicrack.cyolito.com/). However, even without tags, it will try to parse out some information from the filename (usually series, issue number, and publication year).

ComicStreamer is very early ALPHA stages, and may be very flakey, eating up memory and CPU cycles. In particular, with very large datasets, filters on the sub-lists (characters, credits, etc. ) can be slow.

#Requirements 

*python 2.7

(via pip):
*tornado
*sqlalchemy > 0.9
*watchdog
*dateutil
*pil
*configobj
*comictagger
   
(Note: on some ubuntu releases it may be better to get PIL from ubuntu apt package "python-imaging", rather than via pip)


#Installation

Just unzip somewhere.

Settings and database are kept in user folder:
    On unix (mac,linux) it's "~/.ComicStreamer"
    On windows "%APPDATA%\ComicStreamer"


#Running

Just run "comicstreamer" in the base folder (on windows you may want to rename it comicstreamer.py)

Open up a web browser to "http://localhost:8888"

*Use "--help" option to list options

*The first run will require at least one folder with comics in it to be passed in.

*Use the "--reset" option to wipe and rebuild the database

