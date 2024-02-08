[Table of Contents](RHCSA/00_RHCSA_Table_of_Contents.md)

# Using `gzip` and `gunzip` to Compress/Decompress Files
* `gzip directory` compresses `directory` into `directory.gz`
* `gunzip` decompresses compressed files

# Using `bzip2` to Compress/Decompress Files
* `bzip2 *` compresses every file in the current directory
* `bzip2 -d *` decompresses every file in the current directory
* `-v` for verbose
* `-9` best possible compression, but takes a little longer
* `bunzip2` is basically `bzip2 -d`

# Using the Tape Archiver (`tar`) Command
* `tar -czvf` archives and compresses a file
	* `-c` creates an archive
	* `-v` for verbose files
	* `-f` lets user specify a file
	* `-z` compress using `gzip` compression
* `tar -tvf` allows for viewing files within an archive
	* `-t` archive
* `tar -xzvf directory.tar.gz` recreates the subdirectory structure for the extracted archive 
	* `-x` means extract