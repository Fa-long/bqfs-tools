bqfs-tools
==========
This repo provides tools related with bqfs/dffs tools. bqfs/dffs is a text file generated
by TI bqSBB or FlashStream. The bqfs/dffs has i2c command sequence that is used to do firmware
update or DataFlash update.

convbqfs.pl
This is a perl script that convert bqfs/dffs file into a C header file. All i2c command sequence
is converted into a big bqfs_cmd_t array. The definition of bqfs_cmd_t is in bqfs_cmd_type.h.
  Usage: 
      convbqfs.pl --input <input file> [--output {output file}] [--line] [--name {array name}]
  Example:
      convbqfs.pl --input bq27320-v008.bq.fs
      convbqfs.pl --input bq27320-v008.bq.fs --output bq27320-v008-image.h
      convbqfs.pl --input bq27320-v008.bq.fs --line
      convbqfs.pl --input bq27320-v008.bq.fs --name bq27320_bqfs_image
      
  
