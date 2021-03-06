---
layout: docs
title: Adding developer repos to your package manager
permalink: /debian/adding-developer-repos-to-your-package-manager/
distribution: debian
version: 8
---

There is often the case when you need to install a package that is not in the package manger officially, or you need a new version which won't get added to the package manager for awhile. Oftentimes times developers bundle their code into a package for one or more distros.

### Bitmask

[such as bitmask](https://bitmask.net/en/install/linux)

```
sudo -s
```

```
echo "deb http://deb.bitmask.net/debian jessie main" > /etc/apt/sources.list.d/bitmask.list
```

```
wget -O- https://dl.bitmask.net/apt.key | apt-key add -
```
```
apt-get update
```

```
apt-get install bitmask leap-keyring
```

To remove

```
sudo -s
apt-get remove bitmask leap-keyring
apt-key del 0x1E34A1828E207901
rm /etc/apt/sources.list.d/bitmask.list
```

---


### Syncthing

This is how the cool peer-to-peer [syncthing](https://syncthing.net) project explains to [add a custom package](http://apt.syncthing.net)

**Add the release PGP keys**

```
curl -s https://syncthing.net/release-key.txt | sudo apt-key add -
```

**Add the "release" channel to your APT sources**

```
echo deb http://apt.syncthing.net/ syncthing release | sudo tee /etc/apt/sources.list.d/syncthing-release.list
```

 **Update and install syncthing**

```
sudo apt-get update
sudo apt-get install syncthing
```
