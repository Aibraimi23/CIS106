#Notes Lecture 06 | Managing Data and File permissions
##Managing Data
* Backup- Copies files and directories to an archive 
* System backup- Use to restore data in case of a system failure or data loss and corruption
* Archive- File containing many other files, each of which is still identified by its filename, owner, permissions, and timestamp 
###Archiving utilities
* Tar(Tape archive)- creates archives by combining files and directories into a single file
* CPIO- Creates an archive, restores files from an archive, or copies a directory hierarchy. The CPIO utility has three modes of operation:
  * Create mode places multiple files into a single archive file
  * Extract mode restores files from an archive
  * Pass-through mode copies a directory hierarchy 
* Ar- Creates, modifies, and extracts from archives
###File Compression
* Gzip, Bzip2, and xz commands are used for compression
* Gzip, Bzip2, and xz compress files in place meaning the original file is deleted after compression
* bzip offers better compression ratios in comparision to gzip
* xz produces better compression ratios than gzip and bzip2
###Useful commands
* gunzip= gzip -d
* bunzip= bzip -d
* unxz= xz -d
###Zip, 7Zip, and rar
* Zip is an archiving and compression utility
* 7zip is an open source, cross-platform and fully-featured file archiver with a high compression ratio
* To use 7zip on linux you need the package: p7zip-full
* RAR is a proprietary archive file format developed by Eugene Roshal. The command unrar allows Linux users to extract rar archives.
##File Permissions
* A file can be owned only by one user and one group
* ls -l shows you the file user owner and group owner
* The /etc/passwd file contains a list of all the users in Linux
* The /etc/group file contains a list of all the groups in Linux
* The chown command is used for changing group owner
###Files vs Directories
###Files
* R(read)
  * Gives users permission to open and view a files contents
* W(write)
  * Gives users permission to open a file and edit it contents
* X(execute)
  * Allows users to run the file
* Directories
  * R(read)
    * Allows users to list a directory's contents with commands such as ls
  * W(write)
    * Allows users to add or remove files and subdirectories
  * X(execute)
    * Allows users to switch to the directory with the cd command
###chmod command
* The chmod command is used to change permissions on files and directories 
* The permissions argument is the information used to change permissions
* The file/directory argument specifies the file or directory you want to change
* You can use the chmod command in two ways to change file permissions:
  * Symbolic Notation 
  * Numeric Notation