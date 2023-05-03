* tar -> used to group multiple files or directories into a single file. Hence, it is especially useful for archiving data. Tar is an abbreviation for Tape Archive. 

* Files created with tar are often called tarballs. This command has a lot of options and features 

* The tar command followed by -c is used to create an archive. 

* The -f is used to specify the name of the tar file to be created. This is followed by the files or directories to be archived. 

* The -tf option followed by the tar file name, is used to see the contents of the tarball. 

* The -xf flag is used to extract the contents from the tarball. 

* Finally, we can also use the -z command to compress the tarball to reduce its size. 



## Compression ##

* Compression is the technique used to reduce the size consumed by a file or a data set. For example, reducing the size of a file or directory on the Linux file system, there are commands which are specifically used for compression.

* Let us now look at three of the popular ones.

   1. bzip2
   2. gzip
   3. xz

* The space of the compressed file created by these three commands depends on a few factors such as the type of data being compressed. The other factors that affect the
size are the compression algorithm used by these commands and the compression level used. 

* The compression command adds a file extension to the file after the operation, namely .bz2, .gz, and .xz. 

* The compressed files can be uncompressed using the commands, 

   1. bunzip2
   2. gunzip
   3. unxz
   
* Tools such as zcat, bzcat and xzcat allow the compressed file to be read without uncompressing them. 
