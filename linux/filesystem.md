= Linux File System =

Any file storage system, whether it’s a CD-ROM, a hard drive or a USB stick, is essentially a device for storing a long chain of 1s and 0s. When we interact with it, however, we don’t see this; instead, we see files, directories, symbolic links and so on. The software that makes the translation for us is called a file system.

The disk may be split up into individual sections, called partitions, each of which can have its own file system – or none at all.  The disk keeps track of its partitions through its partition table, which tells it how many partitions there are, and where each one begins and ends.

Partitioning tools:
* [[cfdisk]]

File names in linux are case-sensitive.
There is no concept of extensions in linux (like image.jpg, even image or image.blabla will work).

* file fileName : info about file type
* man hier :show file system hierarchy

* [[searching_files]] (find, xargs, grep)
* [[linux_links]]
* [[navigating_linux_filesystem]]




