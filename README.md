# exp-gds

The following is a quick-test to measure the total time to perform "NUM_READS" over fixed size array of length "ARRAY_SIZE", using gds and mmap.

It has been tested with the features from Products graph in the Stanford OGB Repository.
```
get_dataset.py
```
will download the zip file, extract the features. It will take < 5 minutes.


To compile all the experiments. This will output gds_read and mmap_read.

```
make 
```

To execute the program.

Note: make sure the drive is mounted in data=ordered for GDS compatiability. 

parameter 1: < FILEPATH >

parameter 2: <NUM_READS>

parameter 3: <ARRAY_SIZE>


For example: 
```
./gds_read /mnt/nvme/feat.bin 10000 100
```
To test for POSIX v.s GDS mode. Turn on/off  properties.force_compat_mode in cufile.json

Similarly,
```
./mmap_read /mnt/nvme/feat.bin 10000 100
```

