---
title: "Up and Running with MonoGame"
tags:
  - monogame
---

*This article is part of a series on MonoGame. Keep watch for more content, and don't panic. There will be more.*

## Who's Mono? Say *what*?

XNA is dead. It has been for a while. Why should you care? Because it's open source replacement, MonoGame, is better. In fact, so useful that it's worth learning for wholly new games with no existing XNA code.


## What makes it so great?

* Implementations of the framework exist for everything from Android to Apple TV, making your code very portable.

* Everything from the actual methods to what the namespaces are called make it super easy to use older XNA code.

## But... Unity?

You might be talking about non-free (mostly freemium) engines with all their nice [legal crap](https://www.unrealengine.com/en-US/eula)... And [then some](https://unity3d.com/legal/terms-of-service). Do you really want that? Maybe if you want to throw together a quick prototype. Or if you want easy scripting. Otherwise, let the MonoGame framework do the heavy lifting, and the artists work on art, not Unity3D. Just my two cents.



Without further ado, allow me to bestow upon you a pretty sweet "Hello, World" game.



## Let's Begin!

### Installation
If you're on Mac or Linux, grab the Mono runtime if you haven't already. 

Also, go ahead and make sure you have at Visual Studio 2010 or above installed, or MonoDevelop 6 ([there's some weirdness surrounding that, though](http://community.monogame.net/t/installing-monogame-3-6-on-linux/8811)). Mac users can use either one. But I say... *[Use Visual Studio, use Visual Studio!](https://www.reddit.com/r/Unity3D/comments/2k0io0/monodevelop_vs_visual_studio_as_a_c_programmer/)*... A discussion for later.

Point your browser over to [the MonoGame downloads page](http://www.monogame.net/downloads). Select the latest version (MonoGame 3.6 as of this writing). Now, download either the VisualStudio installer for Windows, the Mac package, or the .run Linux installer.
![The MonoGame Download Page](https://i.imgur.com/BP16NbE.png)

#### A note for Linux users.
The rest of the installation should be trivial on Windows and Mac, but if you're not a Linux geek, you might need to do this to be able to execute the installer script:

```
$ chmod +x monogame-sdk.run
```
Now run it:
```
$ sudo ./monogame-sdk.run
```

---
Now, the MonoDevelop/Visual Studio templates should show up in the new project menu:
![MonoGame Visual Studio Templates](https://i.imgur.com/bkxKUlp.png)