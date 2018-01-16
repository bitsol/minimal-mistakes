---
title: "Raspberry Pickings: Choosing and using a Raspberry Pi"
tags:
  - raspberrypi
published: false
---
When you want to build an embedded hardware project, or just purchase a cheap board for its possibilities, you should turn to the Raspberry Pi.
## Why?
At this point, you're probably asking yourself why you should even bother using a Raspberry Pi. Here are some **pros** of using this particular full Linux system board.

### Pros

- Power. If you want to stack multiple projects, or run a few services (such as GPIO [General Purpose Input Output] + Bluetooth + a web and SSH [Secure Shell] server) that use some computing power, the Raspberry Pi is your friend.
- Price. The Arduino is expensive, but one might purchase a clone for as cheap as $5. If you plan to use one of those small $5 microcontrollers, chances are you would benefit more from a stripped-down OS running on a (still tiny) $10 Raspberry Pi Zero W. How would you benefit? Read on.
- IO. 40 pin slots. You get 8 ground pins, 4 power pins, and 28 Input/Output pins with some special interfaces for communication, and a lot of room to grow. Connect LEDs to an output and ground, or button devices and sensors to an input and ground pin. More on pin headers later.
- Wireless. Pretty much all of the latest-gen Pis include Wi-Fi and Bluetooth. Enough said.
- Linux. You can do anything on a PC, they say. Raspberry Pi computers run Linux, I say. You can do anything.
- Price. Pis range from $5 to around $35 for the bare board.
### Cons

- Price. This is listed as a con because of buying limits on the Pi Zero. More on that later.
- Bulky. The form factor of the Pi ~Zero~ makes one slightly less portable than a microcontroller (which can fit anywhere).
## Which One?
You really should only be worrying about a couple models.
### [Raspberry Pi Zero](https://www.adafruit.com/product/2885) ([W](https://www.adafruit.com/product/3400))
![Raspberry Pi Zero](https://cdn-shop.adafruit.com/1200x900/3400-00.jpg)
This tiny $10 thing packs a real punch.

You get 512 MB of RAM, a 1 GHz core, and a flexible form factor that could even fit in a [mint tin](https://blog.adafruit.com/2016/03/04/mintypi-a-pi-zero-based-gaming-system-in-a-mint-tin-piday-raspberrypi-raspberry_pi/).
#### Purchasing
[Adafruit](https://www.adafruit.com) sells these at the MSRP: $5 for the regular, and $10 the wireless board. However, this comes with one caveat: you can only purchase one at a time.

For a long time, the only way to buy multiple Pi Zeros at once (without incurring over $5 in shipping fees each time) was to walk into [Micro Center](http://www.microcenter.com/product/486575/zero_w). *And then leave, and then walk back in, and then leave...*

Then, when the Raspberry Pi Foundation [announced](https://www.raspberrypi.org/blog/zero-wh/) a new model of the Pi Zero with a pre-soldered pin header, we all got a lucky break. How? Now you have a couple options. You can...

- Bundle up. Get anything ranging from the most [barebones](https://www.adafruit.com/product/3409) to the [complete starter](https://www.adafruit.com/product/3411) bundles from Adafruit or elsewhere.
- Buy this:
 - ![Raspberry Pi Zero WH](https://www.raspberrypi.org/app/uploads/2018/01/770A4886-500x333.jpg) 
 - *Now I don't have to solder my fingers together just to attach cool things to my Pi.*
 - The Pi Hut [sells this presoldered Pi Zero WH](https://thepihut.com/products/raspberry-pi-zero-wh-with-pre-soldered-header) for the somewhat premium price of £13.40 (~$18). And yes, you can buy more than one.

#### Problems
It's underpowered (but much more powerful than the average microcontroller), and the ports are all mini-sized, requiring adapters galore to use it in a desktop fashion. But you wouldn't use it as a desktop, would you?

So far we have a simply *more powerful* ~microcontroller~ Linux desktop.
So, how can we justify the cost? You get a powerhouse (one that only costs pennies a year worth of energy) that can do much more than an Arduino, stack more projects, pay one-third of the cost for an official board, have more powerful software configurations, not rely on another PC to get started, and play around with 40 IO pins.

What if you **do** want a "desktop" rival? What if you want to do even more? Read on...

### [Raspberry Pi 3](https://www.adafruit.com/product/3055)
![Raspberry Pi 3](https://cdn-shop.adafruit.com/970x728/3055-06.jpg)
The Raspberry Pi third-gen [Model B flagship board](https://www.raspberrypi.org/products/raspberry-pi-3-model-b/) is my weakness. What can justify paying $35 instead of $10?

A quad-core (it can do all the things), 1.2 GHz Broadcom CPU and 1 GB of RAM. *And*, of course, wireless on board.

*No purchasing problems here.*
*Support the Pi Foundation today. Operators are standing by.*

### Bonus: [Compute Module](https://www.adafruit.com/product/3440)
![Compute Module](https://cdn-shop.adafruit.com/970x728/3440-00.jpg)
A flexible card containing all that yummy Pi goodness in a slim form factor. And, the one type of board I don't own. It's more for industrial stuff, such as putting a Pi in space.

The one linked and shown above happens to be the Compute Module 3, and it looks much easier to fit in small spaces than the Pi 3:
![Raspberry Pi 3](https://www.raspberrypi.org/app/uploads/2017/05/Raspberry-Pi-3-462x322.jpg)

Problem:

*Where are my IO pins???*

I hear you loud and clear. Putting a Pi in space, as I'm sure you're going to do someday, requires many devices. And I hate to say this, but to get the pins you need (for putting a Pi in space) it'll cost you almost $115.

*Yipes. What are you even talking about?*

![Compute Module I/O Board v3](https://cdn-shop.adafruit.com/970x728/3442-00.jpg)
This beast gets you 120 pins.

*Ummm, I don't even need that many.*

Nerds, hop on over to the schematics and 