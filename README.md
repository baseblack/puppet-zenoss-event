puppet-zenoss-event
===================

Create zenoss events from Puppet runs - even masterless ones.

##Synopsis
This is a noddy python script that when started using the included
old skool init script (read: "upstart is pants") will daemonize 
itself. Whilst lurking in the background, puppet-zenoss-event will
use inotify to check when the puppet

##Caveat emptor - you get what you pay for
The code itself works and is tested. No effort has been spent
to make this easy to install on anything by Ubuntu - and even
then it is left to the reader to figure out how to automate
the install. Might I recommend [fpm](https://github.com/jordansissel/fpm/)?

The code is quite naive - read it and see. There are config
variables to set by hand. If there is interest, I can tidy things up
but at the moment this is Good Enough.

Cheerio,

Paul
