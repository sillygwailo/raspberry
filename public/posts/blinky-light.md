##[Blinky Light](/posts/blinky-light)

Along with [my Arduino mission accomplishments](http://arduino.justagwailo.com/), I wanted to dust off the Raspberry Pi that had been sitting unused for over a year. After much yak shaving to get the OS installed, I set it aside while trying to figure out a way to see anything. Recently, a friend <a href="https://twitter.com/beanjammin/status/376603658713964544">tipped me off</a> about a Raspberry Pi getting started night at the Vancouver Hack Space. 

It was a fun atmosphere. In [the introductory blog post for the event](http://vancouver.hackspace.ca/wp/2013/09/07/getting-started-with-raspberry-pi-wednesday-sep-11th-2013/), the hackspacers recommended that we might need our own keyboard and mouse. Not having a USB keyboard, I secured one from Vancouver's Free Geek (as well as a composite wire), then proceeded to the hackspace (with a detour to Hawker's Delight for dinner) to get setup. I did not need the keyboard, as there was a keyboard at the station to get the Raspberry Pi's OS initially setup and to determine the IP address assigned to it on the network.

<a href="http://www.flickr.com/photos/sillygwailo/9770051664/" title="Raspberry Pi OS welcome"><img src="http://farm6.staticflickr.com/5474/9770051664_d775eb1c3b_b.jpg" style="width: 100%" alt="Raspberry Pi OS welcome screen" /></a>

<a href="http://www.flickr.com/photos/sillygwailo/9770053656/" title="Raspberry Pi"><img src="http://farm8.staticflickr.com/7296/9770053656_2250fc717a_b.jpg" style="width: 100%" alt="Raspberry Pi" /></a>

Once hooked back up to the network and headless (not hooked up to a monitor), I was able to SSH through the Vancouver Hack Space's network to the Pi in and download the WebIDE software. Borrowing some lead wires and an LED, and after some initial confusion about where I was to get the Python code responsible, I was able to successfully blink an LED light.

<style>.embed-container {position: relative; padding-bottom: 120%; padding-top: 30px; height: 0; overflow: hidden;} .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='//instagram.com/p/eJYSrlO9Sk/embed/' frameborder='0' scrolling='no' allowtransparency='true'></iframe></div>

The next day, I hooked the Raspberry Pi to my TV at home (with the aforementioned composite wire). And it booted!

<a href="http://www.flickr.com/photos/sillygwailo/9769850332/" title="Raspberry Pi booted on my TV"><img src="http://farm8.staticflickr.com/7366/9769850332_57891c023a_b.jpg" style="width: 100%" alt="Raspberry Pi booted on my TV" /></a>

With a long ethernet cable, I hooked the Pi to my local network (which is nothing more than an Airport Extreme router). After using the same method as at the hackspace to determine the IP address on the local network, I unhooked the TV and the long wire, and hooked up a shorter Ethernet cable to the router. Following that, I was able to SSH into the Pi via my laptop as well as my iPad. Copying over some SSH keys and adding a section in ~/.ssh/config I'm able to login without a password.

Ideas for what's next:

* Punch a hole in the firewall so that the Pi can accept inbound connections from the Internet, or probably just my VPS located in California
* Create a daemon that responds to pings from my VPS every time a specified action occurs. 
    * My first idea for the "specified action" is a unique visit to my website. (I get few enough visits that there should be measurable time between the action.)
* Write code on the Pi to light up an LED when that action occurs. Bonus points for fade in/fade out.
* Have the Raspberry Pi interact wirelessly, either with my home network or directly to my iPhone. Products like <a href="http://www.amazon.com/PLANEX-Bluetooth3-0-IEEE802-11n-corresponding-BT-Micro3H2X/dp/B00644FV14">a combo Bluetooth/Wi-fi adatpter</a> look interesting.

I have two short books that should also dislodge some ideas from my brain: <a href="http://www.packtpub.com/raspberry-pi-networking-cookbook/book"><i>Raspberry Pi Networking Cookbook</i></a> by Rick Golden and the <a href="http://shop.oreilly.com/product/0636920023371.do"><i>Getting Started with Raspberry Pi</i></a> by Matt Richardson and Shawn Wallace. Like with my Arduino missions, I'll stick closely to the book at first, jotting down plans for more adventurous configurations as I go along.
