#Notes Lecture 05 | Command Line Text Editors
##The basics of Nano
###Opening and Creating files
* For opening and creating files
  * nano + filename
###Saving and exiting 
* If you want to save the changes you've made ctrl + 0
* To exit nano, type ctrl + X
* If you ask nano to exit from a modified file, it will ask you if you want to save it, just press N for no and Y for yes. It will then ask for a filename and press enter
###Cutting and pasting
* To cut a single line, you can use ctrl +k the line disappears
* To paste it, use ctrl + U
###Searching for text
* Searching for string is east as long as you think "Whereis" instead of "Search" Simply hit ctrl + W type in you string and press enter
##The basics of VIM
* The vi command is now linked to the vim command, so even when you issue the vi command, you're actually starting the vim editor
* To install vim 
  * sudo apt install vim
###How to start and quit vim
* To start vim typ vim
* To quit vim press esc and type :qa!
  * : prefix for entering command line mode
  * q short for quit 
  * a short for all buffers
  * ! force
  * :qa! quit all now
* To set line numbers :set number
###Vim modes
* Insert mode: used for writing texts
* Normal mode: used for manipulating text
* Command mode: used for entering vim commands
* Visual mode: used for navigation and manipulation of text selections
* Select mode: similar to visual mode
* Ex-mode: Similar to the command-line mode but optimized for batch processing
###Editing a file with vim
* You can tell vim that you want to edit another file by using the e command
* :e new,txt will now open new.txt and allow you to edit
* ctrl + g will show the file that you are currently editing in the status line
* You can also use :f in command mode to see the file that you are currently working on
###Searching words in vim
* Use / and the word you are looking for to search forward
* Letter n will repeat the search for the next word
* ? To search backward 
* *will search for the next occurrence of the word under the cursor
* #will search backward for the previous occurrence of the word under the cursor
###Moving to Lines
* To move to a specific line use : plus the line number
  * :8 will move you to line 8
  * Additionally use 8G
* $ will move to the end of the line
* 0 will move to the beginning of the line
* + executes any vim command from the shell prompt 