# Custom mLinux images for The Things Network

These are custom
[mLinux](http://www.multitech.net/developer/software/mlinux/) images
for the [Multitech](http://www.multitech.com) [MultiConnect®
Conduit™](http://www.multitech.net/developer/products/multiconnect-conduit-platform/)
and [MultiConnect® Conduit™
AP](http://www.multitech.net/developer/products/multiconnect-conduit-access-point/)
built for use as [The Things
Network](https://console.thethingsnetwork.org/) gateways.

For details on how these images differ from the standard images, see
the appropriate branch in [meta-ttni
layer](https://github.com/IthacaThings/meta-ttni).  For example, for
mLinux 3.x see the [mlinux-3
branch](https://github.com/IthacaThings/meta-ttni/tree/mlinux-3)

Note that these images are no longer being updated to github as they exceed the recommended size restrictions.  They are available at https://ttni.tech/mlinux/images

# Usage

To install one of these images on a Conduit or Conduit AP, download
the relevent image for your hardware. The subdirectories below the
version are named _mtcdt_ for Conduit images and _mtcap_ for Conduit
AP images.

```
root@mtcdt:~# cd /var/volatile
root@mtcdt:~# wget https://ttni.tech/mlinux/images/mtcdt/5.3.0b/ttni-base-image-mtcdt-upgrade.bin
root@mtcdt ~# /usr/sbin/mlinux-firmware-upgrade ${PWD}/ttni-base-image-mtcdt-upgrade.bin
```
For a Multitech Conduit Access Point, substitute *mtcap* for *mtcdt* in above lines.

Note that by in some many, most of the configuration of you Conduit or
Conduit AP is lost when doing a firmware upgrade. So perform an
upgrade *before* configuring your device or be prepared to
reconfigure.  
If you use the _Ansible configuration for managing Conduits_ noted below, configuration should be preserved.

# See Also

+ [mLinux layer for building these images](https://github.com/IthacaThings/meta-ttni)
+ [Ansible configuration for managing Conduits](https://github.com/IthacaThings/ttn-multitech-cm)
+ [Container environment for building mLinux on newer system](https://hub.docker.com/r/jchonig/mlinux-be/)
