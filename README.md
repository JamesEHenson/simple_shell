Description
My Shell is a simple UNIX command interpreter that replicates functionalities of the simple shell (sh). Additional functions are also included. This program was written entirely in C as a milestone project for Holberton School.
Installation
Clone this repository into your working directory. For best results, files should be compiled with GCC and the following flags: -Wall -Wextra -Werror -pedantic format.
Usage
After compilation, the resulting program can run stand-alone, either in interactive or non-interactive mode.
Interactive Mode
In interactive mode, simply run the program and wait for the prompt to appear. From there, you can type commands freely, exiting with either the "exit" command or ctrl-D.
Non-Interactive Mode
In non-interactive mode, echo your desired command and pipe it into the program like this:
echo "ls" | ./shell
In non-interactive mode, the program will exit after finishing your desired command(s).
Included Built-Ins
Our shell has support for the following built-in commands:
Command	  Definition
exit [n]  Exit the shell, with an optional exit status, n.
Env  Print the environment.
setenv [var][value]	Set an environment variable and value. If the variable exists, the value will be updated.
unsetenv [var]		Remove an environment variable.
cd [dir] Change the directory.
help [built-in]	Read documentation for a built-in.
The following built-in commands may be supported in future versions:
Command	      Definition
Alias	      Set an Alias.
History	      View the history of the shell.
Outside Programs
My shell can run outside programs by typing their absolute paths (/bin/ls) or the executable name (ls), IF their directory is included in the PATH.
Examples
$ ls -l
total 8
drwxrwxr-x 1 vagrant vagrant Apr 2 13:23 directory_1
drwxrwxr-x 2 vagrant vagrant Apr 2 20:30 directory_2
$ /bin/pwd
/home/vagrant/shell
$ hello world
./hsh: 1: hello: not found
$ help env
env: env
         Print the environment.
Included Files
	 main.c - functions for calling the shell and initializing the shell struct
	 shell.c - functions for running the basic shell logic
	 shellhelp.c - functions for helping the shell run
	 splitstring.c - functions for splitting string from the user
	 stringhelp.c - functions for manipulating strings
	 stringhelp2.c - functions for manipulating strings
	 builtins.c - functions for built-ins
	 builtinhelp.c - functions for helping the built-in functions
	 help.c - functions for the help built-in
	 help2.c - functions for the help built-in
	 cd.c - functions for the cd built-in
	 cd2.c - functions for the cd built-in
	 getenv.c - functions for getting elements from the environment
	 env.c - functions for the env, setenv, and unsetenv built-ins
	 func.c - linked list functions
	 func2.c - linked list functions
	 chpath.c - functions for checking the path of an executable
	 errorhand.c - functions for dealing with errors
	 free.c - functions for freeing allocated memory
	 holberton.h - header file
