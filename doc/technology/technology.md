# Technology

In this document we give a high level technical overview of CloudFleet. Using
CloudFleet consists of three main components:

- the Blimp hardware - a physical machine used as your Blimp
- the Blimp software - the open source software running on your Blimp
- CloudFleet services - a set of online services we provide to make the setup
and usage of your Blimp easy and safe

## Hardware

You can get a pre-packaged CloudFleet Blimp from us or you can setup
your own hardware or VM as a Blimp. When you purchase your Blimp from us you
get this device that you just plug into your router and power and it is
ready for use:

![The CloudFleet Blimp photo](img/blimp.jpg)

Hardware changes fast, so it's possible that these specs might change soon,
but this is the current hardware overview.
The main hardware platform offered as the CloudFleet Blimp (and supported for
those who want to "build their own lightsaber") is a Raspberry Pi 2 Model B.
The machine's specification is:

- 900MHz quad-core ARM Cortex-A7 CPU
- 1GB RAM

Additional components that we package with the Blimp are:

- Custom case with CloudFleet branding
- 8 GB boot Micro SD card
- 16 GB storage USB
- Encryption USB key
- Ethernet & power cables

We also test our software on Debian amd64 VMs, we have some Solidrun Cuboxes
that mostly work and we are open to patches if
you would like to add support for some other hardware platforms.

## Software

In a way, the CloudFleet Blimp is your personal data center
and the Blimp software includes all the web applications being
served from this data center to you.

### Openness

All of the CloudFleet Blimp software is open source. This is a precondition
for security – if you cannot inspect the code that is manipulating your data,
how can you be sure what is it doing with it? It is of course not necessary for
every person to inspect the source code, but the possibility of willing people
being able to do so is a huge step forward in ensuring transparency and openness
of CloudFleet as a privacy-protecting cloud platform.

All of the software that we develop that is running on the Blimp is open source
and licensed under the
[GNU AGPLv3 license](https://www.gnu.org/licenses/agpl-3.0.html).

![AGPLv3 logo](img/agplv3-155x51.png)

CloudFleet is also all about bringing you the best of the open source world
in an easy-to-use device. It includes existing open source code such as:

- the Debian GNU/Linux OS - GNU GPL
- Mailpile - GNU AGPLv3 the Explain the open source part, the license, transparency.

### Architecture

Explain the general architecture with Docker containers for automatic upgrades.

![architecture diagram](img/architecture.png)

### Startup Workflow

Explain the first startup workflow and that the private encryption key gets
generated only when the user first boots their Blimp

![](img/startup.png)

### Access

#### Domain

#### Pagekite

No port forwarding setup necessary! We want CloudFleet to be a plug-and-play
experience. To make this work we partnered with the developers of
[Pagekite](pagekite.net).

![](img/pagekite.png)

### Security Overview

#### HTTPS Connection

Explain the TLS cert registration (mention Let's Encrypt support in the future)

#### Pretty Good Privacy

Mailpile supports easy-to-use PGP encryption of email.

#### Full Disk Encryption

Encrypted with your own private encryption USB key.
[Read more](disk-encryption.html).

#### Zero-Knowledge Backups

### Independent Usage

We believe in freedom and because of this we want to give people as much liberty
as possible in their Blimp usage.

Explain how people can use the Blimp open source software on their own hardware
or VM.

## CloudFleet Services

CloudFleet provides a set of centralised services to our subscribers to make
the usage of your CloudFleet Blimp simpler and safer. These services are
optional.

- explain the CloudFleet services on a high level and why we charge for them

- domain registration
- software upgrades & security patches (via GitHub and
  our private Docker registry)
- pagekite for global access
- zero-knowledge backups
- public-IP mail relay for white-listed email transport (mail servers from
  dynamic IP addresses are often blacklisted as spam by other mail providers)
