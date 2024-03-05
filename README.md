# EXT2 FileSystem in C/Kernel

In this lab, I successfully implemented the following EXT2 filesystem image that the kernel could mount. It is a 1 MiB ext2
file system with 1000 sized blocks and has a space for 128 inodes. The EXT2 filesystem has 4 inotes: the root directory,
lost+found directory, a regular file named hello+world, and a symbolic link named hello that points to the regular file.

## Building

Do make first, then ./ ext2-create

## Running

Do dumpe2fs cs111 -base.img to help debug your EXT2 filesystem
Also do fsck.ext2 cs111 -base.img to debug your EXT2 filesystem and make sure that it's correct

Then, once your filesystem is correct, make a directory called mnt. Then do sudo mount -o loop cs111-base.img mnt to
mount your EXT2 filesystem and what loop does is it let you use the file.

## Cleaning up

Unsudo your mount by doing sudo umount mnt when you're done.
Remove the mount by rmdir mnt to delete the directory mnt when you're done.
make clean
