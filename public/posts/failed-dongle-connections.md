## [Failed Dongle Connections](/posts/failed-dongle-connections)

<blockquote class="twitter-tweet" lang="en"><p>These two USB dongles should open up some possibilities for my Raspberry Pi. <a href="http://t.co/qzTl5y6Ncy">pic.twitter.com/qzTl5y6Ncy</a></p>&mdash; Richard Eriksson (@sillygwailo) <a href="https://twitter.com/sillygwailo/statuses/442532428045758464">March 9, 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

No luck tonight on getting my Bluetooth and Wi-Fi USB dongles working. Despite [the excellent instructions by James Nebeker and David G. Young on getting the software setup](http://developer.radiusnetworks.com/2013/10/09/how-to-make-an-ibeacon-out-of-a-raspberry-pi.html), my dongle does not support Bluetooth LE to begin with. If you're getting

<code>Can't set advertise mode on hci0: Connection timed out (110)</code>

...after you've arrived at typing in

<code>hciconfig hci0 leadv 3</code>

...the best explanation I can offer is that your Bluetooth dongle doesn't support LE.

The end goal here is to make a beacon where stuff happens (the opening up of possibilities) based on my proximity to my Raspberry Pi, as determined by my iPhone 5. The following look useful once I get the proper dongle:

 * [A node.js library for creating, discovering, and configuring iBeacons](https://github.com/sandeepmistry/node-bleacon)
 * [Tracking mobile BlueTooth LE iBeacon engagements with Node.js](https://github.com/mschmulen/tracking-bluetooth-ibeacons-with-node)

Once I get a dongle that's compatible with LE, that is. At least I won't have to do the Bluez software compilation again.

Connecting the Wi-Fi dongle was met with the same result: a failure to connect. On the plus side, some learning about how I can setup my network, and a <code>apt-get update</code> and a <code>apt-get upgrade</code> to get the latest and greatest of everything.

I found the following links helpful:

* [How to Setup Wi-Fi On Your Raspberry Pi via the Command Line](http://www.howtogeek.com/167425/how-to-setup-wi-fi-on-your-raspberry-pi-via-the-command-line/)
* [Getting WiFi on a Headless Raspberry Pi](http://milkandtang.com/blog/2013/08/27/getting-wifi-on-a-headless-raspberry-pi/).
* [Raspberry Pi Stack Exchange question on the subject](http://raspberrypi.stackexchange.com/questions/11631/wifi-setup-for-multiple-networks)
* [Realtek wifi 8188CUS doesn't "just work"](http://www.raspberrypi.org/forum/viewtopic.php?f=28&t=52236)

I'm grateful to my past self for properly setting up the Ethernet connection with a static IP address, an entry in <code>~/.ssh/config</code> on my laptop, and SSH keys. This ensured that any mistakes made to my networking settings would be confined to the <code>wlan0</code> section and not lock me out of my Pi.
