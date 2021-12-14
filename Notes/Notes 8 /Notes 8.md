# Shell Scripting
* Source code vs machine code
  * Source code is the human readable code written in a programing language like python
  * Machine code consists of binary 1s and 0s and is the language a computers CPU understands
* Compiler: a program used for converting a complete source code into machine code
* Interpreter: a program that converts source code into machine code line by line
* Compiled program vs Interpreted program
  * a compiled is a binary file produced by a compiler
  * an interpreted program is a program that requires an interpreter to interpret and run each instruction 
* Shell scripts are examples of interpreted programs, and the interpreter used is the BASH shell
### Creating a basic script
* Start vim, enable line numbers, and enter insert mode
* type:
  * #!/bin/bash
  * echo "this is a script that displays information about your linux system"
  * uname -a
* Save the file and name it script1.sh
* Type chmod u+x script1.sh to make the file executable 
* to run the script type : ./script1.sh
### Displaying text
* To display a line of text use the echo command
  * Ex. echo "this is a message"
* echo -n does not output a new line
## Working with variables
* Variable: placeholder for data
* Environment variable: is the placeholder for data that can change: typically, it gets its value automatically from the OS startup or the shell being used.
* The HOME environment variable stores the absolute pathname to a user's home directory, so it varies for each user
* The env command allows you to see all environment variables
* You can also used the echo command to see the calue of each environment variable
  * echo $HOME
  * echo $HOST
### Exit Status Codes
* Exit Status code: a number sent to the shell when you run a command
* Successful commands usually return the code 0, and failures return a value greater than 0
## Using Structured Commands
### Conditions
* The if statement is used to carry out certain commands based on testing a condition and the exit status of the command
* if-statement- Starts the condition being tested
* then statement- Starts the portion of code specifying what to do if the condition evaluates to true
* else statement- Starts the portion of code specifying what to do if the condition evaluates to false.
* The fi statement indicates the end of the if statement
![attributeOperators](../Notes%208%20/AO.png)
![NumericComparison](../Notes%208%20/NC.png)
![StringComparison](../Notes%208%20/SC.png)
