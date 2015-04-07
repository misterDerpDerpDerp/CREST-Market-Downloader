# CREST-Market-Downloader
Python (wx python) based market downloader. 

This fetches data from EVE Online's Crest API and outputs in a format that Navbot can process. No more clicking that export button! All you have to do is select a filter file that contains a list of item ids whose data you want to fetch and output the files to your marketlog folder using this script's options. Then let navbot do its job.

UPDATE: I have hard coded the regionID and solarsystemIDs for Jita, Rens, Amarr and Dodixie instead of creating a list of every single system and region with their corresponding stations because those are the few trade hubs I use. Apologies for the cop out! I'll gladly add a proper list to this code if someone can write it out. :P

Requires:
* python 2.something
* wx python
* requests

You need to set up your own application in the developers site, and fill in details into downloader.ini appropriately.

The callback url on the developers site is http://localhost:[port from downloader.ini]/

Now also needs a cacert.pem file in the same directory as the script. In part, so it packages nicely with pyinstaller.

The filter file format is one typeid per line.
To clear the filter, once set, go to the filter dialog and hit cancel.
