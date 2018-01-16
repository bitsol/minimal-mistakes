---
title: "Raspberry Pickings: Choosing and using a Raspberry Pi"
tags:
  - raspberrypi
published: true
---
When you want to build an embedded hardware project, or just purchase a cheap board for its possibilities, you should turn to the Raspberry Pi.
## Why?
At this point, you're probably asking yourself why you should even bother using a Raspberry Pi. Here are some **pros** of using this particular full Linux system board.

### Pros

- Power. If you want to stack multiple projects, or run a few services (such as GPIO [General Purpose Input Output] + Bluetooth + a web and SSH [Secure Shell] server) that use some computing power, the Raspberry Pi is your friend.
- Price. The Arduino is expensive, but one might purchase a clone for as cheap as $5. If you plan to use one of those small $5 microcontrollers, chances are you would benefit more from a stripped-down OS running on a (still tiny) $10 Raspberry Pi Zero W. How would you benefit? Read on.
- IO. 40 pin slots. You get 8 ground pins, 4 power pins, and 28 Input/Output pins with some special interfaces for communication, and a lot of room to grow. Connect LEDs to an output and ground, or button devices and sensors to an input and ground pin. More on pin headers later, and hardware in later posts.
- Wireless. Pretty much all of the latest-gen Pis include Wi-Fi and Bluetooth. Enough said.
- Linux. You can do anything on a PC, they say. Raspberry Pi computers run Linux, I say. You can do anything.
- Price. Pis range from $5 to around $35 for a bare board.

### Cons

- Price. This is listed as a con because of buying limits on the Pi Zero. More on that later.
- Bulky. The form factor of the Pi ~Zero~ makes them slightly less portable than a microcontroller (which can come in all shapes and sizes).
## Which One?
You really should only be worrying about a couple models.
### [Raspberry Pi Zero](https://www.adafruit.com/product/2885) ([W](https://www.adafruit.com/product/3400))
![Raspberry Pi Zero](https://cdn-shop.adafruit.com/1200x900/3400-00.jpg)

This tiny $10 thing packs a real punch.

You get 512 MB of RAM, a 1 GHz core, and a great form factor that could even fit in a [mint tin](https://blog.adafruit.com/2016/03/04/mintypi-a-pi-zero-based-gaming-system-in-a-mint-tin-piday-raspberrypi-raspberry_pi/).
#### Purchasing
[Adafruit](https://www.adafruit.com) sells these at the MSRP: $5 for the regular, and $10 the wireless board. However, this comes with one caveat: you can only purchase one at a time.

For a long time, the only way to buy multiple Pi Zeros at once (without incurring over $5 in shipping fees each time) was to walk into [Micro Center](http://www.microcenter.com/product/486575/zero_w). *And then leave, and then walk back in, and then leave, and then walk back in.*

Then, when the Raspberry Pi Foundation [announced](https://www.raspberrypi.org/blog/zero-wh/) a new model of the Pi Zero with a pre-soldered pin header, we all got a lucky break. How? Now you have a couple options. You can...

- Bundle up. Get anything ranging from the most [barebones](https://www.adafruit.com/product/3409) to the [complete starter](https://www.adafruit.com/product/3411) bundles from Adafruit or [elsewhere](https://www.amazon.com/CanaKit-Raspberry-Wireless-Starter-Official/dp/B06XJQV162/ref=sr_1_4?ie=UTF8&qid=1516122403&sr=8-4&keywords=Raspberry+Pi+Zero+W).

or...
- Buy this:

  ![Raspberry Pi Zero WH](https://www.raspberrypi.org/app/uploads/2018/01/770A4886-500x333.jpg) 
  - *Now I don't have to solder my fingers together just to attach hardware to my Pi.*
  - The Pi Hut [sells this Pi Zero WH](https://thepihut.com/products/raspberry-pi-zero-wh-with-pre-soldered-header) with a presoldered header (more on those later) for the somewhat premium price of £13.40 (~$18). And yes, you can buy more than one.

or just...
 - Walk into Micro Center.

*Solomon notes: I have actually requested that Adafruit stock the Pi Zero WH, as at the time of writing the only sellers of this model are UK-based.*

*We will see what purchasing quantities Adafruit will have available when the time comes.*
#### Problems
It's underpowered (but much more powerful than the average microcontroller), and the ports are all mini-sized, requiring adapters galore to use it in a desktop fashion. But you wouldn't use it as a desktop, would you?

And... one may consider this an inconvenience: the non-WH Zero doesn't come with a GPIO pin header. More on that later.

So far we have a simply *more powerful* ~microcontroller~ Linux desktop.

So, how can we justify the cost?

For the deal, you get a powerhouse that only costs pennies a year worth of energy.

What if you **do** want a "desktop" rival? What if you want to do even more with a better CPU? Read on...

### [Raspberry Pi 3](https://www.adafruit.com/product/3055)
![Raspberry Pi 3](https://cdn-shop.adafruit.com/970x728/3055-06.jpg)

The Raspberry Pi third-gen [Model B flagship board](https://www.raspberrypi.org/products/raspberry-pi-3-model-b/) is my weakness. What can justify paying $35 instead of $10?

A quad-core, 1.2 GHz Broadcom CPU and 1 GB of RAM. *And*, of course, wireless on board.

*No purchasing problems here. You're welcome.*

*Support the Pi Foundation today. Operators are standing by.*

### Bonus: [Compute Module](https://www.adafruit.com/product/3440)
![Compute Module](https://cdn-shop.adafruit.com/970x728/3440-00.jpg)

According to the Raspberry Pi Foundation, "The Compute Module 3 is a Raspberry Pi 3 in a more flexible form factor, intended for industrial application[.]"

The Compute Module shown above looks much easier to cram into small spaces than the Pi 3:

![Raspberry Pi 3](https://www.raspberrypi.org/app/uploads/2017/05/Raspberry-Pi-3-462x322.jpg)

Q&A:

*Where are my IO pins???*

I hear you loud and clear. Putting a Pi in space, as I'm sure you're going to do someday, requires many a device, which requires many an IO pin.

I hate to say this, but to get the pins you need (for putting a Pi in space) it'll cost you almost $115.

*Yipes. What are you even talking about?*

![Compute Module I/O Board v3](https://cdn-shop.adafruit.com/970x728/3442-00.jpg)

"The Compute Module IO Board V3 is a development kit for those who wish to make use of the Raspberry Pi in a more flexible form factor." (Raspberry Pi Foundation, n.d.)

This beast gets you 120 pins.

*Ummm, I don't even need that many.*

Engineers, hop on over to the [schematics](https://github.com/raspberrypi/documentation/tree/master/hardware/computemodule) and fabricate a custom PCB [with less pins](https://github.com/deltabeard/cmio).

If you don't know what I'm talking about (at least I don't), then maybe you won't need the Compute Module anyway.

## Next Steps

### IO Pins on the Zero

If you are purchasing a Raspberry Pi Zero or Zero W and want to connect hardware, you'll need to buy a header and solder it on.

![Male GPIO Header](https://cdn-learn.adafruit.com/assets/assets/000/028/768/medium640/raspberry_pi_2822-00.jpg?1448520203)

I highly recommend a classic [male header](https://www.adafruit.com/product/2822) (shown above), which gives the most connection strength. Combined with some [jumper wires](https://www.adafruit.com/product/1950), your Pi will be ready for anything.

### Headless Setup
When you purchase a board (especially the Zero), don't expect it to function on its own without adapters and peripherals.

As my next few posts will be about creating embedded hardware with the Pi, you might want to follow [Adafruit's guide](https://learn.adafruit.com/raspberry-pi-zero-creation/overview) to setting up a headless OS, no adapters required.

## Wrapping Up
With a Raspberry Pi computer, you can do much more than with an Arduino-like microcontroller:
- Stack more projects.
- Pay one-third of the cost for an official board.
- Have more powerful software configurations.
- Don't rely on another PC to get started.
- Play around with 40 IO pins.

Purchase a Pi Zero for extra tinyness, a Pi 3 for pure computing power, or a Compute Module for industrial work.

We learned about some purchasing problems surrounding the Pi Zero and complication on the IO board for the Compute Module.

### What do I even need?
To get a Raspberry Pi functioning as its own desktop computer (if you aren't running it [headless](https://learn.adafruit.com/raspberry-pi-zero-creation/overview)), you'll need a few things:

- A monitor + HDMI cable.
- A keyboard and mouse.
- An SD card.
- Another computer to [flash the SD card](https://learn.adafruit.com/setting-up-a-raspberry-pi-with-noobs/overview) with your chosen operating system or the New Out Of the Box Software (NOOBS) installer, if it isn't pre-flashed already.
- A 5v mobile micro-USB power supply.

For the Zero you'll also need...
- A mini-HDMI to HDMI adapter.
- A micro-USB OTG cable and USB hub.
- A GPIO header and soldering iron (optional, and not even required with the Zero WH)

### What's Next?
Up next are some posts on interfacing and building Pi hardware, making IoT (Internet of Things) devices with the Pi, and maybe even soldering (if I'm up to the task).

## References
