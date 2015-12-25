# Technology

*In this document we give a high level technical overview of CloudFleet.*

## Hardware

Raspberry Pi 2 Model B. Specification:

- 900MHz quad-core ARM Cortex-A7 CPU
- 1GB RAM

Additional components

- Custom case with CloudFleet branding
- 8 GB boot Micro SD card
- 16 GB storage USB
- Encryption USB key
- Ethernet & power cables

## Software

### Openness

Explain the open source part, the license, transparency.

### Architecture

Explain the general architecture with Docker containers for automatic upgrades.

### Startup Workflow

Explain the first startup workflow and that the private encryption key gets
generated only when the user first boots their Blimp

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

- domain
- pagekite
- 0-knowledge backups
