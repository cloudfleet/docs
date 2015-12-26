# Full Disk Encryption

The source code for our LUKS initialisation process
can be found [here][cryptpart]. After the disks are encrypted, two partitions
are created on them:

 - the encrypted swap partition
 - the encrypted storage partition

The storage partition is formatted as BTRFS, a copy-on-write filesystem,
and two subvolumes are created on it:

- a data storage subvolume - */opt/cloudfleet/data*
- a Docker storage subvolume - */var/lib/docker*

The encryption USB key has to be plugged into the Blimp when it is booting in
order to decrypt these partitions for normal usage. After the boot procedure is
finished, the user should remove the encryption USB key and keep it in a safe
location to keep the data secure in case of Blimp theft.

[cryptpart]: https://github.com/cloudfleet/blimp-engineroom/tree/master/bin/cryptpart "cryptpart"
