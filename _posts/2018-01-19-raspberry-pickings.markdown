---
title: "Raspberry Pickings: Choosing and Using a Raspberry Pi"
tags:
  - raspberrypi
published: true
---
We [already know](https://bitsol.github.io/why-pi/) that you should use a Raspberry Pi for most hardware projects. Now you may ask the question...
## Which One?
You really should only be worrying about a couple models.
### [Raspberry Pi Zero](https://www.adafruit.com/product/2885) ([W](https://www.adafruit.com/product/3400))
<img src="https://cdn-shop.adafruit.com/1200x900/3400-00.jpg" height="450" width="600" alt="Raspberry Pi Zero">

*Source: [Adafruit](https://www.adafruit.com/product/3400).*

This tiny $10 thing packs a real punch. Don't have a ton of space for your project? Get the Zero.

You get 512 MB of RAM, a 1 GHz core, and a great form factor that could even fit in a [mint tin](https://blog.adafruit.com/2016/03/04/mintypi-a-pi-zero-based-gaming-system-in-a-mint-tin-piday-raspberrypi-raspberry_pi/).
#### Purchasing
[Adafruit](https://www.adafruit.com) sells these at the MSRP: $5 for the regular, and $10 the wireless board. However, this comes with a caveat: you can only purchase one at a time.

Why do the Raspberry Pi resellers place buying limits? A Raspberry Pi engineer named James Hughes seems to be the most active in the community on this topic.

As Hughes (2017) [has stated](https://www.raspberrypi.org/forums/viewtopic.php?f=63&t=176662#p1221364): "You can buy Zero's in quantity, if you commit to large scale purchasing (1000's), and you will pay more than the individual price (i.e. > $10 for the Pi0W). Basically, a deal with the Foundation."

This implies that the Foundation makes a very small profit margin off the Zero at the $10 price, and the quantity is limited to encourage people to purchase the more expensive models.

Still, there are ways to get around this with certain resellers without incurring multiple shipping charges by:

- Walking into a Micro Center store and purchasing them at an [ever increasing rate](http://www.microcenter.com/product/486575/Zero_W).
- Bundling up. Get anything ranging from the most [barebones](https://www.adafruit.com/product/3409) to the [complete starter](https://www.adafruit.com/product/3411) bundles from Adafruit or [elsewhere](https://www.amazon.com/CanaKit-Raspberry-Wireless-Starter-Official/dp/B06XJQV162/ref=sr_1_4?ie=UTF8&qid=1516122403&sr=8-4&keywords=Raspberry+Pi+Zero+W).
- Purchasing the [Raspberry Pi Zero WH](https://www.raspberrypi.org/blog/zero-wh/):

  ![Raspberry Pi Zero WH](https://www.raspberrypi.org/app/uploads/2018/01/770A4886-500x333.jpg) 

  *Source: [Raspberry Pi Foundation Blog.](https://www.raspberrypi.org/blog/zero-wh/)*
  
  "*Now I don't have to solder my fingers together just to attach hardware to my Pi.*"
  - The Pi Hut [sells this](https://thepihut.com/products/raspberry-pi-zero-wh-with-pre-soldered-header) Pi Zero model with a presoldered GPIO header for the somewhat premium price of £13.40 (~$19). And yes, you can buy more than one.

*Solomon notes: I have actually requested that Adafruit stock the Pi Zero WH, and at the time of writing the only sellers of this model are UK-based. We will see what purchasing quantities Adafruit will have available when the time comes.*

#### IO Pins on the Zero

If you are purchasing a Raspberry Pi Zero or Zero W and want to connect hardware, you'll need to buy a GPIO pin header and solder it on.

<img src="https://cdn-learn.adafruit.com/assets/assets/000/028/768/medium640/raspberry_pi_2822-00.jpg?1448520203" height="240" width="320" alt="Break-away 0.1 2x20-pin Strip Dual Male Header">

*Source: [Adafruit](https://www.adafruit.com/product/2822).*

As Adafruit's founder and owner, Limor Fried, has quipped: "Like blue jeans and Coca-Cola, the 2x20 male header is the classic option." (Fried, 2015)

A [male header](https://www.adafruit.com/product/2822) gives the most connection strength when combined with some [jumper wires](https://www.adafruit.com/product/1950) that have at least one female connector.

#### Problems
It's underpowered (but much more powerful than the average microcontroller), and the ports are all mini-sized, requiring adapters galore to use it in a desktop fashion. But you wouldn't use it as a desktop, would you?

So far we have a small Linux microcomputer that I'm telling you can replace microcontrollers in most situations, but what if you **do** want a "desktop" rival? What if you want to do even more with a better processor? Read on...

### [Raspberry Pi 3](https://www.adafruit.com/product/3055)
<img src="https://cdn-shop.adafruit.com/970x728/3055-06.jpg" height="364" width="485" alt="Raspberry Pi 3">

*Source: [Adafruit](https://www.adafruit.com/product/3055).*

The Raspberry Pi third-gen [Model B flagship board](https://www.raspberrypi.org/products/raspberry-pi-3-model-b/) is my weakness. What can justify paying $35 instead of $10?

A quad-core, 1.2 GHz Broadcom processor and 1 GB of RAM. *And*, of course, wireless on board.

*No purchasing problems here. You're welcome.*

*Support the Pi Foundation today. Operators are standing by.*

### Bonus: [Compute Module 3](https://www.adafruit.com/product/3440)
<img src="https://cdn-shop.adafruit.com/970x728/3440-00.jpg" height="364" width="485" alt="Raspberry Pi Compute Module 3">

*Source: [Adafruit](https://www.adafruit.com/product/3440).*

According to the Raspberry Pi Foundation, "The Compute Module 3 is a Raspberry Pi 3 in a more flexible form factor, intended for industrial application[.]"

The Compute Module 3 shown above (which even has 4GB of flash memory onboard) looks much easier to cram into small spaces than the Pi 3.

Q&A:

*Where are my IO pins???*

I hear you loud and clear. Putting a Pi in space, as I'm sure you're going to do someday, requires many a device, which requires many an IO pin.

I hate to say this, but to get the pins you need (for putting a Pi in space) it'll cost you almost $115.

*Yipes. What are you even talking about?*

<img src="https://cdn-shop.adafruit.com/1200x900/3442-00.jpg" height="600" width="450" alt="Raspberry Pi Compute Module I/O Board V3">

*Source: [Adafruit](https://www.adafruit.com/product/3442).*

"The Compute Module IO Board V3 is a development kit for those who wish to make use of the Raspberry Pi in a more flexible form factor." (Raspberry Pi Foundation, n.d.)

This beast gets you 120 pins. That's a ton of space-age sensors you can control right there, sonny boy.

*Ummm, I actually don't even need that many.*

Engineers, hop on over to the [schematics](https://github.com/raspberrypi/documentation/tree/master/hardware/computemodule) and fabricate a custom PCB [with less pins](https://github.com/deltabeard/cmio).

If you don't know what I'm talking about (I don't), then maybe you don't need the Compute Module anyway.

## Next Steps

### Headless Setup
When you purchase a board (especially the Zero), don't expect it to function on its own without adapters and peripherals.

As my next few posts will be about creating embedded hardware with the Pi, you may want to follow [Adafruit's guide](https://learn.adafruit.com/raspberry-pi-zero-creation/overview) to setting up a headless OS with no adapters required.

## Wrapping Up
With a Raspberry Pi computer, you can do much more than with an Arduino-like microcontroller:
- Stack more projects.
- Pay one-third of the cost for an official board.
- Have more powerful software configurations.
- Don't rely on another PC to get started.
- Play around with 40 IO pins.

Purchase a Pi Zero for extra compactness, a Pi 3 for pure computing power, or a Compute Module for industrial work.

We learned about some purchasing problems surrounding the Pi Zero and complication on the IO board for the Compute Module.

### What do I even need?
To get a Raspberry Pi functioning as its own desktop computer (if you aren't running it [headless](https://learn.adafruit.com/raspberry-pi-zero-creation/overview)), you'll need a few things:

- A monitor + HDMI cable.
- A keyboard and mouse.
- A micro SD card.
- Another computer to [flash the SD card](https://learn.adafruit.com/setting-up-a-raspberry-pi-with-noobs/overview) with your chosen operating system or the New Out Of the Box Software (NOOBS) installer, if it isn't pre-flashed already.
- A 5V mobile micro-USB power supply (think: high-quality Android charger).

For the Zero you'll also need:
- A mini-HDMI to HDMI adapter.
- A micro-USB OTG (On The Go) cable and USB hub.
- (Optional) GPIO header and soldering iron (not required with the Zero WH)

### What's Next?
Up next are some posts on interfacing with hardware on the Pi, making IoT (Internet of Things) devices, and maybe even soldering (if I'm up to the task).

Until next time...
## References
### Quotes
Fried, Limor. (2015, October 26). GPIO header options. In *Introducing the Raspberry Pi Zero*. Retrieved from [https://learn.adafruit.com/introducing-the-raspberry-pi-zero/gpio-header-options](https://learn.adafruit.com/introducing-the-raspberry-pi-zero/gpio-header-options).

Hughes, J. (2017, October 11). Re: use pi zero w in commercial production [Forum post]. Retrieved from [https://www.raspberrypi.org/forums/viewtopic.php?f=63&t=176662#p1221364](https://www.raspberrypi.org/forums/viewtopic.php?f=63&t=176662#p1221364).

### Images
Raspberry Pi Zero W [Digital image]. (n.d.). Retrieved from [https://www.adafruit.com/product/3400](https://www.adafruit.com/product/3400)

Raspberry Pi Zero WH [Digital image]. (n.d.). Retrieved from [https://www.raspberrypi.org/blog/zero-wh/](https://www.raspberrypi.org/blog/zero-wh/)

Break-away 0.1" 2x20-pin Strip Dual Male Header [Digital image]. (n.d.). Retrieved from [https://www.adafruit.com/product/2822](https://www.adafruit.com/product/2822)

Raspberry Pi 3 [Digital image]. (n.d.). Retrieved from [https://www.adafruit.com/product/3055](https://www.adafruit.com/product/3055) 

Raspberry Pi Compute Module 3 [Digital image]. (n.d.). Retrieved from [https://www.adafruit.com/product/3440](https://www.adafruit.com/product/3440)

Raspberry Pi Compute Module I/O Board V3 [Digital image]. (n.d.). Retrieved from [https://www.adafruit.com/product/3442](https://www.adafruit.com/product/3442)


Did you actually scroll down this far? I got nothing more to show you. Sorry.
