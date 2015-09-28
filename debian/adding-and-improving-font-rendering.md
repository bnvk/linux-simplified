---
layout: docs
title: Adding & Improving Font Rendering
permalink: /debian/adding-and-improving-font-rendering/
distribution: debian
version: 8
---


Installing MS TrueType fonts in Ubuntu

You can install the MS core fonts by installing the msttcorefonts package. You will need to enable the â€œUniverseâ€ component of the repositories (done by default in Feisty & Hardy). After that, run the following from the command line:

```
sudo apt-get install ttf-mscorefonts-installer
```

While this gives you the core fonts, it also gives you the ability to install any other font by simply copying the .TTF to the ~/.fonts/ directory.


```
sudo fc-cache -fv
```

For some of the popular fonts that ship with Mac OS X, you’ll have to go through a somewhat more complex process to install them. Please note that for educational and professional environments (minus graphic design and similar fields), you will more than likely not need these fonts, as much of the world depends on Microsoft’s fonts, specifically Times New Roman. However if you would like to have these on your Ubuntu system, you’ll need to open up your terminal and enter in the following commands:


Download a .tar package with the fonts.

wget http://dl.dropbox.com/u/26209128/mac_fonts.tar.gz

    “Unzips” the .tar package.

    tar zxvf mac_fonts.tar.gz

Move the font files into the system’s fonts folder

```    
sudo mv fonts /usr/share/fonts/
```

When installing new fonts, you’ll need to re-login to be able to see & use them. Optionally, this step can be bypassed by regenerating the fonts cache with:

```
sudo fc-cache -f -v
```


Original source: [makeuseof.com](http://www.makeuseof.com/tag/how-to-get-mac-and-windows-fonts-in-ubuntu-linux/)
