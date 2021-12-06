#Notes Lecture 04 | Manipulating files and directories
##Creating directories 
* mkdir is used for creating a single directory or multiple directories
* to create multiple directories, separate each directory name with a space
* You can create directories in the present working directory or in a different directory by using an absolute path or relative path
##Creating files
* touch command is used for creating files
* Create a file called list - touch list
##Deleting files and directories
###rm command
* rm removes files
* rm by default does not remove directories. To remove a directory use rm with -r option
* In linux and other Nix systems you cannot remove non empty directories 
* To remove empty directories use the rmdir command 
* To remove non-empty directories use rm -r + directory name or directory absolute path
##Moving files and directories
###The mv command
* mv moves and renames directories
* The basic formula of the mv command is:
  * mv + source + destination
* Where source is the file or directory that you want to move and destination is where the directory or file is going
* Both source and destination can be an absolute path or relative path 
##Copying files and directories
###The cp command
* cp copies files/directories from source to a destination 
* The cp command uses the same structure as the mv command
  * cp + files to copy + destination 
* To copy directories you must use the -r option
  * cp -r + directory to copy + destination
##Getting Help
* Man pages are documentation files that describe Linux shell commands, executable programs, system calls, special files, and so forth
* Man Pages are quick references 
* To view a man page type: man + command
* To exit the man page press letter "q"
* Most commands have a help a help option built in. Normally that option is -h or --h or --help
* Some commands my not have a man page but an info page
* You can use the whatis command to display a simple description of what a command does
##Working with Wildcards
* Wildcard represent letters and characters used to specify a filename for searches
* File globbing is the processing of pattern matching using wildcards
* The wildcards are officially called metacharater wildcards
###The * Wildcard
* The main wildcard is a star, or asterisk (*) character
* A start alone matches anything and nothing and matches any number of charaters
###The ? Wildcard
* The ? wildcard metacharacter matches precisely one character
* In addition, the question mark proves very useful when working with hidden files
* If you want to list all hidden files you can use: ls ..??* which will match all files that start with a . or .. abd have any character after it.
###The [ ] Wildcard 
* The brackets wildcard match a single character in a range
* The brackets wildcard wildcard use the exclamation mark to reverse the match.For example, match everything except the vowels [!aeiou] or any other character except numbers [!0-9]
###Brace Expansion
* Brace expansion {} is not a wildcard but another feature of bash that allows you to generate arbitrary strings to use with commands