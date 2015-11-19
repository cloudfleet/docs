# Getting Started for Hackers

You want to use your own hardware or a virtual machine?
You're at the right place! If you just want to use the CloudFleet Blimp,
better go [here](quickstart.html) instead.

TODO: quickest possible way to get started for hackers, with any potential
side-stories being linked to elsewhere in the docs.

**Assuming Raspberry Pi 2 (dm-crypt modules for the Cubox not set up
automatically)**

## Order a CloudFleet service subscription

Go to <https://cloudfleet.io/order.html>, fill out your domain info.

TODO: allow the upload of a OTP (or allow downloading of a random OTP and
allow for e.g. a device labeled cf-otp to be
plugged into the blimp on the first boot and use that
instead of the mac address)


## Set up your domain's DNS

TODO: make option to "use your own existing domain"

*Maybe also move this to another page as an optional route
"CloudFleet with your own domain"*

Steps to set up a custom domain with a new Cubox:

 - register a domain (e.g. Namecheap)
 - point your blimp.<domain> DNS to CloudFleet's Pagekite frontend
   (the . in the end may or may not be necessary depending on your registrar)

        <type>  <host>  <value>
        CNAME   blimp   myblimp.net.

 - point your domain's MX record to cloudfleet.cloudfleet.io

        <type>  <host>  <value>                     <priority>
        MX      @       cloudfleet.cloudfleet.io.   1


## Prepare the Blimp's SD card

TODO: Explain how to burn the "golden image".

If you want to setup everything on a Debian Linux from scratch
(for transparency or you maybe want to use an existing server),
follow [the detailed explanation](debian.html)
of how to run Ansible playbooks to install everything.

TODO: add the OTP somehow

## Prepare the key and storage USB devices

In the [blimp repository](https://github.com/cloudfleet/blimp),
in the *scripts* folder is a script to format two
USB devices with correct labels. It expects a key device path (e.g. /dev/sda)
and a storage device path (e.g. /dev/sdb) **Warning: running this script on the
provided devices will erase all data on them. Be sure to back up everything
important!**

In Linux, run:

    ./scripts/format_usbs.sh <key device> <storage device>

Plug the USB devices into the device.

(on the next reboot the devices will be set up for our LUKS encrypted
partition scheme)

This script is also available on the Blimp itself (if you ssh into it) and can
be run as:

    /opt/cloudfleet/engineroom/bin/cryptpart/wipe_disks.sh <key device> <storage device>

(typically, on the blimp, the 1st USB you plug in will be /dev/sda
and the 2nd /dev/sdb, to help you visually distinguish them)
