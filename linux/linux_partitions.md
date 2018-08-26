= Partitions =

A hard drive can be divided into sections (partitions). The information is stored in a
`Partition Table` scheme such as MBR or GPT. Partition tables are created by
tools like `fdisk` and `parted`.

Once created, a partition must be formatted with an appropriate file system
(swap excepted) before data can be written to it.

To print/list existing partitions (of specific device like /dev/sda):
`parted /dev/sda print` or `fdisk -l /dev/sda`

Types of partition table:
1. Master Boot Record (MBR)
2. GUID Partition Table (GPT)

`MBR` is the first 512 bytes of a storage device. It contains an operating
system bootloader and the storage device's partition table. It plays an
important role in the boot process under `BIOS` systems.

Thre are 3 types of partitions in the MBR scheme:
* Primary
* Extended
  * Logical

`Primary` partitions can be bootable and are limited to 4 partitions per disk.

`Extended` partitions can be thought of as containers for `logical`
partitions. A hard disk can contain no more one extended partition. The
extended partition is also counted as a primary partition. The number of
logical partitions residing in an extended partition is unlimited.

The customary numbering scheme is to create primary parititions `sda1` through
`sda3` followed by an extended partition `sda4`. The logical partitions on
`sda4` are numbeted `sda5`, `sda6`, etc.


GUID Partition Table (`GPT`) is a partitioning scheme that is part of the
Unified Extensible Firmware Interface specification; it uses globally unique
identifiers (GUIDs), or UUIDs in the Linux world, to define partitions and
partition types. It is designed to succeed the MBR. You can have arbitrary 
number fo partitions in GPT.

== Sources ==
[[https://wiki.archlinux.org/index.php/Partitioning|Partitioning]]
