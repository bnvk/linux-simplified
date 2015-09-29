---
layout: docs
title: Playing back audio & video files
permalink: /fedora/playing-back-audio-video-files/
distribution: fedora
version: 21
---

#### Install all the necessary codecs

```
sudo yum -y install gstreamer-plugins-bad gstreamer-plugins-bad-free-extras gstreamer-plugins-bad-nonfree gstreamer-plugins-ugly gstreamer-ffmpeg
```

And then do these as well. Why these need to be done separately, not sure!

```
sudo yum -y install gstreamer1-libav gstreamer1-plugins-bad-free-extras gstreamer1-plugins-bad-freeworld gstreamer1-plugins-base-tools updates gstreamer1-plugins-good-extras gstreamer1-plugins-ugly gstreamer1-plugins-bad-free gstreamer1-plugins-good gstreamer1-plugins-base gstreamer1
```

Now install playback tools: ffmpeg, Mencoder, ffmpeg2 theora, Mplayer

```
yum -y install ffmpeg mencoder ffmpeg2theora mplayer
```

Original source: [askfedoraproject.org](https://ask.fedoraproject.org/en/question/27881/help-i-cannot-play-a-dvd-in-videos-or-vlc-player-in-fedora-18/)
