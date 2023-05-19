## How to fix "No usable free extent could be found" error when running DISKPART

 
![No Usable Free Extent Could Be Found Error When Running DISKPART !!INSTALL!!](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRIjjt5IVDg3InHpJIbaMkc_Uuk9WEZjh3xlv7hxU0vJifyu8ilcUX-JAlE)

 ```html 
# How to fix "No usable free extent could be found" error when running DISKPART
 
If you are trying to create a partition on a disk using the DISKPART command-line tool, you may encounter an error message that says "No usable free extent could be found. It may be that there is insufficient free space to create a partition at the specified size and offset. Specify different size and offset values or don't specify either to create the maximum sized partition. It may be that the disk is partitioned using the MBR disk partitioning format and the disk contains either 4 primary partitions, (no more partitions may be created), or 3 primary partitions and one extended partition, (only logical drives may be created)."
 
## No usable free extent could be found error when running DISKPART


[**Download Zip**](https://www.google.com/url?q=https%3A%2F%2Furllie.com%2F2tLEr4&sa=D&sntz=1&usg=AOvVaw2oNRLgeaglQ0GL7uwlQ-Dp)

 
This error can occur for various reasons, such as:
 
- The disk has no unallocated space or the unallocated space is too small to create a new partition.
- The disk is using the MBR partition style and has reached the limit of 4 primary partitions or 3 primary partitions and 1 extended partition.
- The disk is corrupted or has bad sectors.

To fix this error, you can try the following solutions:
 
## Solution 1: Extend the unallocated space
 
If the disk has some unallocated space but it is not enough to create a new partition, you can try to extend the unallocated space by shrinking an existing partition. To do this, follow these steps:

1. Open Disk Management by pressing Windows + R keys, typing diskmgmt.msc and hitting Enter.
2. Right-click on the partition that you want to shrink and select Shrink Volume.
3. Enter the amount of space that you want to shrink in MB and click Shrink.
4. This will create some unallocated space next to the partition that you shrunk. You can then use DISKPART to create a new partition on the unallocated space.

## Solution 2: Convert the disk to GPT
 
If the disk is using the MBR partition style and has reached the limit of 4 primary partitions or 3 primary partitions and 1 extended partition, you can try to convert the disk to GPT (GUID Partition Table) which supports up to 128 partitions per disk. However, this will erase all the data on the disk, so make sure you back up your important files before proceeding. To convert the disk to GPT, follow these steps:

1. Open Command Prompt as administrator by pressing Windows + X keys and selecting Command Prompt (Admin).
2. Type diskpart and hit Enter.
3. Type list disk and hit Enter. This will show you all the disks connected to your computer.
4. Type select disk n and hit Enter, where n is the number of the disk that you want to convert.
5. Type clean and hit Enter. This will delete all the partitions and data on the selected disk.
6. Type convert gpt and hit Enter. This will convert the selected disk to GPT.
7. You can then use DISKPART to create new partitions on the converted disk.

## Solution 3: Check and repair the disk
 
If the disk is corrupted or has bad sectors, it may cause errors when running DISKPART. You can try to check and repair the disk using the CHKDSK command-line tool. To do this, follow these steps:

1. Open Command Prompt as administrator by pressing Windows + X keys and selecting Command Prompt (Admin).
2. Type chkdsk /f /r x: and hit Enter, where x is the drive letter of the disk that you want to check and repair.
3. This will scan and fix any errors or bad sectors on the selected disk. It may take some time depending on the size of the disk.
4. After CHKDSK finishes, you can try to run DISKPART again and see if the error is resolved.

  ``` 0f148eb4a0
