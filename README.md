# Custom mLinux images for The Things Network

These are custom
[mLinux](http://www.multitech.net/developer/software/mlinux/) imagex
for the [Multitech](http://www.multitech.com) [MultiConnect®
Conduit™](http://www.multitech.net/developer/products/multiconnect-conduit-platform/)
and [MultiConnect® Conduit™
AP](http://www.multitech.net/developer/products/multiconnect-conduit-access-point/)
built for use as [The Things
Network](https://console.thethingsnetwork.org/).gateways.

For details on how these images differ from the standard images, see
the appropriate branch in [meta-ttni
layer](https://github.com/IthacaThings/meta-ttni).  For example, for
mLinux 3.x see the [mlinux-3
branch](https://github.com/IthacaThings/meta-ttni/tree/mlinux-3)

# Usage

To install one of these images on a Conduit or Conduit AP, download
the relevent image for your hardware. The subdirectories below the
version are named _mtcdt_ for Conduit images and _mtcap_ for Conduit
AP images.

```
root@mtcdt:~# wget https://github.com/IthacaThings/mlinux-images/raw/master/3.13.3/mtcdt/ttni-base-image-mtcdt-upgrade-withboot.bin
root@mtcdt ~# /usr/sbin/mlinux-firmware-upgrade /home/root/ttni-base-image-mtcdt-upgrade-withboot.bin
```

Note that by default, most of the configuration of you Conduit or
Conduit AP is lost when doing a firmware upgrade. So preform an
upgrade *before* configuring your device or be prepared to
reconfigure.
