#Alfred 2 Flush DNS Workflow

Flush the DNS cache in Mac OS X (10.7+).

![](https://raw.github.com/cdraeger/alfred2-flushdns-workflow/master/screenshots/keyword.png)

##Download

For an easy installation, you can download the exported workflow here: [flushdns.alfredworkflow](export/flushdns.alfredworkflow?raw=true)

##Usage

###Keyword: `fdns`

No arguments will prompt you for a user and password.

For more convenience, you can also enter your password after the keyword (separated by a space). This is much quicker, and don't worry: this workflow does not store or submit any data. If the password happens to be wrong, you will see the regular prompt by the system.

Success or errors are reported through a notification.

Command used (see [Apple Support](http://support.apple.com/kb/HT5343)): 
  `sudo killall -HUP mDNSResponder || sudo dscacheutil -flushcache`

##Changelog

####v1.0
Initial release
