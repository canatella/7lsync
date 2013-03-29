7lsync
======

7lsync is a simple ruby script to retreive and maintain a copy of your
music collection fron http//www.7digital.com. Just run it once with
the directory where to put your collection, it will ask for your
7digital credentials and start downloading your collection. Then you
can put it in a cron job without any argument and when you buy new
title, they will be downloaded.

It works by storing the last date where it did an update, comparing it
to the purchase date of your tracks to minimize bandwidth.

Installing
----------

It needs ruby > 1.9.0 and the mechanize gem.

Usage
-----

First setup the configuration and do a first synchronisation manually

    7lsync /where/to/store/the/files

Then add a cron job

    (crontab -l; echo "30 17 * * * 7lsync") | crontab -

To reset the config or download all your collection again:

    rm ~/.7lsync.yml
