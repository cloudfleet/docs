# Technology

In this document we give a high level technical overview of CloudFleet. Using
CloudFleet consists of three main components:

- the Blimp hardware - a physical machine used as your Blimp
- the Blimp software - the open source software running on your Blimp
- CloudFleet services - a set of online services we provide to make the setup
and usage of your Blimp easy and safe

You can get a pre-packaged CloudFleet Blimp from us or you can install the Blimp
on your own hardware or VM.

## Hardware

Hardware changes fast, so it's possible that these specs might change soon,
but this is the current hardware overview.
The main hardware platform supported for our Blimp is a Raspberry Pi 2 Model B.
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

### Openness

Explain the open source part, the license, transparency.

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
- software upgrades & security patches
- pagekite for global access
- zero-knowledge backups
