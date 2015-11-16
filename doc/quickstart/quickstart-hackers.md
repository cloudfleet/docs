# Getting Started for Hackers

You want to use your own hardware or a virtual machine?
You're at the right place! If you just want to use the CloudFleet Blimp,
better go [here](quickstart.html) instead.

TODO: quickest possible way to get started for hackers, with any potential
side-stories being linked to elsewhere in the docs.

**Assuming Raspberry Pi 2 (dm-crypt modules for the Cubox not set up
  automatically)**

## Prepare the Blimp's SD card

TODO: Explain how to burn the "golden image" with a
[link](https://github.com/cloudfleet/blimp#blimp) to a detailed
explanation on how to run Ansible playbooks to explicitly install everything
(for transparency and reproducibility) on a vanilla Debian Linux.

## Prepare the key and storage USB devices

Also in the blimp repository, in the *scripts* folder is a script to format two
USB devices with correct labels. It expects a key device path (e.g. /dev/sda)
and a storage device path (e.g. /dev/sdb) **Warning: running this script on the
provided devices will erase all data on them. Be sure to back up everything
important!**

In Linux, run:

    ./scripts/format_usbs.sh <key device> <storage device>

Plug the USB devices into the device.

(on the next reboot the devices will be set up for our LUKS encrypted
partition scheme)
