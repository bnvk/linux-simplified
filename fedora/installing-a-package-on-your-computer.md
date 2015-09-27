---
layout: docs
title: Working with packages on your computer
permalink: /fedora/working-with-packages-on-your-computer/
distribution: fedora
version: 21
---

On Fedora a compiled package exists with an `.rpm` file extension.

#### Installing a package from a file

```
rpm -Uhv package_file.rpm
```

---

#### To remove a package (called erase in RPM terminology)

```
rpm e package_name
```
