puppet-zenoss-event
===================

Create zenoss events from Puppet runs - even masterless ones.

##Synopsis
This is a noddy python script that when started using the included
old skool init script (read: "upstart is pants") will daemonize 
itself. Whilst lurking in the background, puppet-zenoss-event will
use inotify to check when a file that suggests a puppet run has failed.
It will then raise an event on a Zenoss instance to that effect.

None of this would be necessary if Puppet didn't abuse return codes.

##Caveat emptor - you get what you pay for
This code might break stuff. But don't blame me, it was Puppet that
chose to break Unix in the first place - I'm just the mopman
cleaning up the mess they left behind.

The code itself works and is tested in production. No effort has been
spent to make this easy to install on anything by Ubuntu - and even
then it is left to the reader to figure out how to automate the
install. Might I recommend [fpm](https://github.com/jordansissel/fpm/)?

The code is quite naive - read it and see. There are config
variables to set by hand. If there is interest, I can tidy things up
but at the moment this is Good Enough.

Cheerio,

Paul
