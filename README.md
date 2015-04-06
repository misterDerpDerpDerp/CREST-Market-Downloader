# CREST-Market-Downloader
Python (wx python) based market downloader. 

This fetches data from EVE Online's Crest API and outputs in a format that Navbot can process. No more clicking that export button! Once it's complete, all you will have to do is select a filter file that contains a list of item ids whose data you want to fetch and output the files to your marketlog folder using this script's options. Then let navbot do its job.

This is in development thanks to Fuzzmeister (who wrote most of this script!) and Nuadi (who helped with getting region and solarsystem ids):

http://www.reddit.com/user/Fuzzmiester http://www.reddit.com/user/nuadi

What needs to be done now is to add Nuadi's region and solarsystem code so it outputs the proper ids instead of the system name.

Requires:
* python 2.something
* wx python
* requests

You need to set up your own application in the developers site, and fill in details into downloader.ini appropriately.

The callback url on the developers site is http://localhost:[port from downloader.ini]/

Now also needs a cacert.pem file in the same directory as the script. In part, so it packages nicely with pyinstaller.


The filter file format is one typeid per line.
To clear the filter, once set, go to the filter dialog and hit cancel.
