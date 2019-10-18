TOPIC: Gonk
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Gonk

Gonk is the lower-level operating system of Firefox OS and consists of a Linux kernel (based on the
[Android Open Source Project](http://source.android.com/) (AOSP))
and userspace hardware abstraction layer (HAL).

The kernel and several of the userspace libraries are common open-source projects: Linux, libusb,
bluez, and so forth. Some other parts of the HAL are shared with AOSP: GPS, camera, and others.
You could call Gonk a very simple Linux distribution.

Gonk is a **porting target** of Gecko (just as Gecko has been ported to OS X, Windows, and Android).
Since Firefox OS has full control over Gonk, we can expose interfaces to Gecko that aren't accessible
on other operating systems, for example the full telephony stack and display frame buffer.

## Learn More

- [Gonk page on the Firefox OS zone](https://developer.mozilla.org/en-US/Firefox_OS/Platform/Gonk)
