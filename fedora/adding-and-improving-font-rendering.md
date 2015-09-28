---
layout: docs
title: Adding & Improving Font Rendering
permalink: /fedora/adding-and-improving-font-rendering/
distribution: fedora
version: 21
---

Improving how fonts render and making things look how they are supposed to look according to creators of websites and various designs is actually a really simple task.

#### 1. Add RPM Fusion Repos

We need this to install Freetype-Freeword engine. In order to do this make sure you have [RPM Fusion repos](http://rpmfusion.org) enabled

#### 2. Freetype

Install Freetype-Freeworld package from RpmFusion. This is a font rendering engine.

```
sudo yum install freetype-freeworld
```

#### 3. Install Microsoft, MacOS or Custom Fonts

There are many common windows fonts like Arial that aren’t distributed in Fedora for policy reason. You can get them from SourceForge

    http://sourceforge.net/projects/corefonts/files/the%20fonts/final/

Then you will need to extract those (.exe files) with Cabextract program. This isn’t in F20 default installation and you need to get it.

Get the extracted TTF files and copy them into:

**System Wide**

```
/usr/share/fonts/msfonts
```

**User Specific**

```
~/.local/share/fonts/msfonts
```

This way you can install any fonts you like.

#### 4. Edit Font Configuration

Open up your `local.conf` file to edit it

```
nano /etc/fonts/local.conf
```

And add the following to this:

```
  <?xml version="1.0"?>
  <!DOCTYPE fontconfig SYSTEM "fonts.dtd">
  <fontconfig>
    <match target="font">
    <edit name="autohint" mode="assign">
      <bool>true</bool>
    </edit>
    <edit name="hinting" mode="assign">
      <bool>true</bool>
    </edit>
    <edit mode="assign" name="hintstyle">
      <const>hintslight</const>
    </edit>
    </match>
  </fontconfig>
```


#### 5. Tweak Fonts Rendering

Open Gnome Tweak Tool, under Fonts Panel and set:

**Hinting ->Slight**

**Antialisiing->Rgba**

#### 6. Reboot & Enjoy!

You can avoid rebooting by updating your fonts with fc-cache command, and restart your session.

This still won’t lead to Ubuntu Font Rendering Standards, but it will greatly improve Fedora’s user experience. Never skip that in Fedora!

As a side not, if you do any web-design, you will certainly need this, because you must match how fonts look like in every system. As far as I know, every system has its very own and unique way to render and display fonts, but this is another story ;)



Original source: [worldofgnome.org](http://worldofgnome.org/how-to-greatly-improve-font-rendering-under-fedora-20/)
