#Alfred 2 Flush DNS Workflow

Flush the DNS cache in OS X (10.9+).

![](https://raw.github.com/cdraeger/alfred2-flushdns-workflow/master/screenshots/keyword.png)

##Download

For an easy installation, you can download the exported workflow here: [flushdns.alfredworkflow](export/flushdns.alfredworkflow?raw=true)

##Usage

###Keyword: `fdns`

No arguments will prompt you for a user and password.

For more convenience, you can also enter your password after the keyword (separated by a space). This is much quicker, and don't worry: this workflow does not store or submit any data. If the password happens to be wrong, you will see the regular prompt by the system.

Success or errors are reported through a notification.

Command used: 

__`sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder`__

If `mDNSResponder` is not available (see [how to flush the DNS cache in OS X Yosemite](http://osxdaily.com/2014/11/20/flush-dns-cache-mac-os-x/)), the following command for `Discoveryd` is used:

__`sudo discoveryutil mdnsflushcache; sudo discoveryutil udnsflushcaches`__

##Changelog

####v1.1
- Updated for compatibility with OS X 10.10 Yosemite
- Improved error handling
- Minimum requirement upped to OS X 10.9 Mavericks (though it might still work on OS X 10.7 / 10.8)

####v1.0
- Initial release
