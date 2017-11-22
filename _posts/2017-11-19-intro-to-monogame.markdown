---
title: "Up and Running with MonoGame"
tags:
  - monogame
published: false
---

*This incomplete article will be expanded and updated every once in a while.*

## Who's Mono? Say *what*?

XNA is dead. It has been for a while. Why should you care? Because it's open source replacement, MonoGame, is better. In fact, so useful that it's even worth learning for wholly new games with no existing XNA code.


## What makes it so great?

* Implementations of the framework exist for everything from Android to Apple TV, making your code very portable.

* Everything from the actual methods to what the namespaces are called make it super easy to use older XNA code.

## But... Unity?

You might be talking about non-free (mostly freemium) engines with all their nice [legal crap](https://www.unrealengine.com/en-US/eula)... And [then some](https://unity3d.com/legal/terms-of-service). Why would anyone want that? Maybe if they want to throw together a quick prototype. Or if they need easy scripting.

Otherwise, let the MonoGame framework do the real heavy lifting for the programmers, and the artists work on art, not Unity3D. Just my two cents.



Without further ado, allow me to bestow upon you a pretty sweet "Hello, World" game.



## Let's Begin!

### Installation
If you're on Mac or Linux, grab the Mono runtime if you haven't already. 

**Disclaimer: I'm going to be using Windows 10 to develop this project. All the examples should be reproducible on other operating systems, but technology changes fast. I'm not promising anything. Sorry.**

Also, go ahead and make sure you have either Visual Studio 2010 or above installed, or MonoDevelop 6 (there's some weirdness surrounding that though. See the next section for a solution.)

 Mac users can use either one. But the people have spoken. You really should [use Visual Studio](https://www.reddit.com/r/Unity3D/comments/2k0io0/monodevelop_vs_visual_studio_as_a_c_programmer/)... A discussion for later.

Point your browser over to [the MonoGame downloads page](http://www.monogame.net/downloads). Select the latest version (MonoGame 3.6 as of this writing). Now, download either the VisualStudio installer for Windows, the Mac package, or the .run Linux installer.
![The MonoGame Download Page](https://i.imgur.com/BP16NbE.png)

#### An important note for Linux users.
For reasons mentioned previously, you're probably using MonoDevelop.

Also mentioned previously and [restated across the Internet](http://community.monogame.net/t/installing-monogame-3-6-on-linux/8811), the ```flatpak``` enviroment used by all the recent versions of MonoDevelop won't work with MonoGame.

To combat this, you can just build MonoDevelop from source or use [@cra0zy's](https://github.com/cra0zy) [script](https://github.com/cra0zy/monodevelop-run-installer) that does all the work of packaging it in a useful format. I've had both work and fail in different situtations, but try the script first. It's so much faster. Thanks, [@cra0zy](https://github.com/cra0zy).

Follow the latest instructions [here](https://github.com/cra0zy/monodevelop-run-installer/blob/master/README.md) for using cra0zy's script, or [build MonoDevelop from source](http://www.monodevelop.com/developers/building-monodevelop/).

After MonoDevelop is all set up, installing MonoGame should be trivial. Set the premissions of the .run script you downloaded earlier...
```
$ chmod +x monogame-sdk.run
```
Now run it...
```
$ sudo ./monogame-sdk.run
```

If there are any dependencies you need, you should be able to install them with ```apt```.


---

After the installation process, the MonoDevelop/Visual Studio templates should show up in the new project menu.

### Getting Around the Place

To make this easier and remove/lessen the need to manage multiple projects and asset references, let's make a new cross-platform OpenGL desktop project:
![MonoGame Visual Studio Templates]({{ "/assets/images/MonoGameTemplates.png" | absolute_url }})

Go ahead and open ```Game1.cs``` if you haven't already. The default code consists of a few important methods:
* ```Initialize()```, for connecting to services or loading non-graphic files. We won't be using it in this example. 
* ```LoadContent()```, for loading content (duh). We'll use this for populating our graphics variables (like the ```Texture2D```s for the sprites).
* ```UnloadContent()``` gets called when the game ends. If you're not using a ```ContentManager``` object (and in this example you won't be), you need to manually [*get rid of*]

[WRITE!!!]