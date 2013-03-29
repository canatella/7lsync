7lsync
======

7lsync is a simple ruby script to retreive and maintain a copy of your
music collection fron http//www.7digital.com. Just run it once with
the directory where to put your collection, it will ask for your
7digital credentials and start downloading your collection. Then you
can put it in a cron job without any argument and when you buy new
title, they will be downloaded.

So in short, first run:

    7lsync /where/to/store/the/files

Then run 

    crontab -l
    
and add

    30 17 * * * 7lsync
    
It needs ruby > 1.9.0 and the mechanize gem.
   
