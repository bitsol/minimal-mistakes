---
title: "No Problemo, GPIO: Overcoming the worst challenges related to Raspberry Pi hardware."
tags:
  - raspberrypi
published: true
---
I've [told you](https://bitsol.github.io/why-pi/) that if you want to build a small embedded hardware project, automate
things in your household, or just purchase a cheap computer for its
possibilities, you should turn to the Raspberry Pi. I've also [shown you](https://bitsol.github.io/raspberry-pickings/)
some of the different models.

A while ago, when I wanted to connect my first [arcade button](https://www.adafruit.com/product/1185) (it *is* massive),
I had no idea where to begin.

Every tutorial on the Internet shows the process with a breadboard. I had a million questions:
1. Do we need to use a breadboard anyway?
2. Why is there even a resistor for an input?
3. Which pins can actually be used for Input/Output?
4. Can someone help me figure out what wires go to what lugs on the microswitch?

It's okay if you didn't understand some of those questions. Why? Because you'll have those questions after buying your first piece
of hardware anyway.

## Essentials
### Pinout
After you've soldered a General Purpose Input Output, or GPIO male (preferred) [header](https://www.adafruit.com/product/2822) in
([or not soldered](https://www.adafruit.com/product/3662) a header in) if required, you may notice that there are no fancy diagrams
telling you what pins can be used for ground, for example.

This is the part where I contradict myself. [pinout.xyz](http://pinout.xyz) provides that diagram, plus an interactive pin "browser", so to speak.

![Pinout.xyz]({{ "/assets/images/pinout.xyz.png" | absolute_url }})

*Screenshot of [pinout.xyz](http://pinout.xyz).*

#### Pin Numberings

Let's understand this. There are three main types of numberings for the actual IO pins.
- BCM (Broadcom SOC channel)
  - These numbers are determined by the Broadcom chip on the Raspberry Pi.
  - Used by the [RPi.GPIO](https://pypi.python.org/pypi/RPi.GPIO) and [gpiozero](https://gpiozero.readthedocs.io/en/stable/) [Python](https://python.org) libraries.
- BOARD
  - The location of the pin on the header, indicated by the numbers next to the pin slots on the diagram.
  - Used by [RPi.GPIO](https://pypi.python.org/pypi/RPi.GPIO), upon request.
- WiringPi
  - [WiringPi](http://wiringpi.com/) is a C GPIO library, with **unofficial** bindings for Python and Java. It uses its own pin numbering, [accessible on pinout.xyz](https://pinout.xyz/pinout/wiringpi), and designed to mimic the Arduino pins.
  - Used by WiringPi. Wasn't that easy to figure out!

So, any given pin is either for supplying or diverting power to/from the Raspberry Pi, configurable as an input or output for any kind of devices, should be reserved for a specific kind of device interface, or can be used for ground. Let's look at a practical example instead of these confusing words, shall we?

### Connecting a Device
To do this, you should be using jumper leads (preferably with female plugs) in your male header. The other end can go to whatever you want.

If you're just digesting this information, you may ask why I'm not using a breadboard (a plastic board with goodies such as a ground rail, typically used for prototyping). The answer is, it's not compact enough for me, and for most small scale projects a full-sized breadboard is overkill.

Mind you, on a breadboard you can hook up a lot more electronics (because of the rails).

If you've never touched electronics before, think of it like this: one side for input or output, and another for ground (to discharge unused voltage).

#### Button Microswitch Time!

This is a microswitch.

<img src="https://cdn-shop.adafruit.com/970x728/473-02.jpg">

*This one is two-legged, as there's no LED. Source: [Adafruit](https://www.adafruit.com/product/473).*


This is another microswitch.

<img src="https://cdn-shop.adafruit.com/970x728/1185-01.jpg">

*Built-in LED + resistor, four legs, and a whole heck of confusion. Source: [Adafruit](https://www.adafruit.com/product/1185).*

They need to be attached to the button somehow, and if that means screwing it in tight, don't be shy!

If you actually read the image captions, you would know that the only reason the second button (100mm)'s microswitch looks so much more complex is because this one has a built in LED.

It's actually pretty straightforward to get these things hooked up, as long as you know which side is which, that is.

#### Identifying Switch Legs

<img src="https://cdn-shop.adafruit.com/970x728/3433-01.jpg">

*Source: [Adafruit](https://www.adafruit.com/product/3433).*

Sometimes it's just trial and error, and other times there are hints and indicators written in the plastic. If you look closely at this image, you'll see that one set of microswitch legs are offset from each other.

That's for the button. How do I know? Look closely at the diagram engraved near the pins and you'll see something that looks like a push switch.

How do I really know?

*The jig is up.*

<img src="https://cdn-learn.adafruit.com/assets/assets/000/042/961/original/3d_printing_arcade-button-pinout.jpg?1498336753">

*Source: [Adafruit Learning System](https://learn.adafruit.com/assets/42961).*

It makes sense, doesn't it? Here's another example of when documentation can save your life:

<img src="https://cdn-learn.adafruit.com/assets/assets/000/028/806/original/gaming_press-your-button-wiring-diagram.png?1448728329">

*Source: [Adafruit Learning System](https://learn.adafruit.com/assets/28806).*

This diagram applies to the four-legged button above. However, common sense can still apply: the one towards the ground goes to ground.

As for the LED polarity (negative and positive), if it's not too obvious, you can just swap the wires around until it lights with your code.

#### A Note on Resistors
To avoid damage to your Pi or LED, you'll need at least a 330-ohm [resistor](https://www.adafruit.com/category/837) wired up (you can just twist the wires) on the positive (longer end) of the LED to make sure nothing explodes.
#### From GPIO Pins to Wires

If you really want this:

![Raspberry Pi Zero with Arcade Button]({{ "/assets/images/arcade-button-rpi.jpg" | absolute_url }})

The Pi side is plug-and-play...

 <img src="https://media.giphy.com/media/xT1R9D1py1eLhevFwk/giphy.gif">

 ...but to get a button hooked up, you can:

- Solder a stripped metal [connector](https://www.adafruit.com/product/266) terminal to each leg.
    - As Mike Stone (2017) of Adafruit Support [said](https://forums.adafruit.com/viewtopic.php?f=50&t=127392#p635313)        to me: "...pull the plastic housing off the female terminal at one end of the wire, flatten the female terminal with a pair of pliers, then solder the flattened part to the switch lug..."
     <img src="https://media.giphy.com/media/3o6nUZLbn2xRPXpkuA/giphy.gif">
- If the button is small enough (unlike the one pictured): take advantage of [quick connects](https://www.adafruit.com/product/1152).
- Simply solder bare copper wire to the legs. <img src="https://cdn-learn.adafruit.com/assets/assets/000/042/969/original/3d_printing_button-pwr-solder.gif?1498340314">

  *Source: [Adafruit Learning System](https://learn.adafruit.com/assets/42969)*

#### Testing Time!
1. Install [```gpiozero```](https://gpiozero.readthedocs.io/en/stable/) on Raspbian with ```apt-get install python-gpiozero python3-gpiozero```, connect the positive end of the LED (if there is one) and button to BCM 21 and BCM 13 respectively (or just change the values in the script). Use the adjacent ground pins to make wiring convenient.

   ![Raspberry Pi Pinout with Arcade Button + LED]({{ "/assets/images/pinout-button-and-led.png" | absolute_url }})

2. Run this Python script:

  ```
  from gpiozero import LED, Button
  led = LED(21)
  button = Button(13)

  button.when_pressed = led.on
  button.when_released = led.off

  pause()
  ```
  The button will light when pressed, and you can replace ```led.on``` with any custom function.
  
  Stay tuned everyone!

## References
### Quote
Stone, M. (2017, December 3). Re: Quick Connects + Massive Arcade button = Works with Rpi [Forum post]. Retrieved from [https://forums.adafruit.com/viewtopic.php?f=50&t=127392#p635313](https://forums.adafruit.com/viewtopic.php?f=50&t=127392#p635313).
### Images
All uncredited images were created exclusively for this post by me. All screenshots of [pinout.xyz](https://pinout.xyz) taken by me.

Arcade Button - 30mm Translucent Red [Digital image]. (n.d.). Retrieved from [https://www.adafruit.com/product/473](https://www.adafruit.com/product/473)

Massive Arcade Button with LED - 100mm Red [Digital image]. (n.d.). Retrieved from [https://www.adafruit.com/product/1185](https://www.adafruit.com/product/1185)

Mini LED Arcade Button - 24mm Green [Digital image]. (n.d.). Retrieved from [https://www.adafruit.com/product/3433](https://www.adafruit.com/product/3433)

3d_printing_arcade-button-pinout.jpg [Digital image]. (n.d.). Retrieved from [https://learn.adafruit.com/assets/42961](https://learn.adafruit.com/assets/42961)

gaming_press-your-button-wiring-diagram.png [Digital image]. (n.d.). Retrieved from [https://learn.adafruit.com/assets/28806](https://learn.adafruit.com/assets/28806)

3d_printing_button-pwr-solder.gif [Digital image]. (n.d.). Retrieved from [https://learn.adafruit.com/assets/42969](https://learn.adafruit.com/assets/42969)
