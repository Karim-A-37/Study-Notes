Linux is treated everything as files with its famous rule, "everything is a file".

so file is file and also directory is treated also as file , that is impressive and very different than other OSs.

we can use two different types of paths:
	Relative path   -->> is the short path like I am in root and I want to open Downloads I can easily write (cd Downloads), in other words relative path is dependent on your current directory.

Absolute path -->> is full path from its root it should starts from [/] because it is root of every file like like I am in root and I want to open Downloads I can easily write (cd /root/Downloads).

in standard Linux file systems (ext4) , the path name of a file, including all / characters, may be no more than 4095 bytes(it is actually 4096 but since one byte is reserved for the null terminator) long are useable, in other words must not exceed 4095 character since character is storing as byte.

Each component of the path name separated by / characters may be no more than 255 bytes long, in other words name of file or directory must not exceed 255 characters.

Linux uses tree hierarchy system to sort or deal with its file, so it is like levels lower levels like 0 is ( / ) and get higher levels for other things and so on, we can say that path is combination of levels and the absolute path should start from path level 0 until reaching the desired path.

here are some special usages for some special cases :
	1- tilde(~) -->> pointer for home directory of user.

2- dot(.) -->> pointer for current directory.

3- double dots(..) -->> pointer of higher directory or previous one in path(like back button).

4- wildcard asterisk( * ) -->> pointer to complete with any characters after or before, like if i want to list anything starts with a I use ls a* and so on.

5- wildcard question mark(?) -->> it is matching for one character in file or directory name, like if i use ls ?

means list all files or directories its name is one character.

6- square brackets ([ ]) -->> if we use ls [ac] it means list files where name is a or c , if we use it [!ac]=[ ^ac]means list files where name isn't a or c.

7- dollar sign($) -->> it can be used with echo command for command substitution echo $(date) and for variable substitution x=5 echo $x and for arithmetic substitution echo $[1+2] or echo $((1+2))
	
	
At this time I have learned more commands to deal with files such as :
	1- cd -->> to change directory, like to go to home of user ( cd ~user ), go to the previous directory that I have opened before current directory ( cd - ).

2- dir -->> to list directory like ls but dir it doesn't separate between files and directories using colors, to make this happen we should add (--color) option.

3- ls -R -->> to list directories and its internal content.

4- ls -r -->> to list by reversing alphabet order.

5- touch -->> to create file, we can create multiple files at the same time but the destination should be directory in this case, if the file exists it will overwrite timestamp, it can't tolerate with the space in the name of file it will treat it like two separate names , to add space we can use ("name" ) or ('name') or (name\ rest of name).

6- mkdir -->> to create directories, it is like touch in the naming process.

7- cp -->> to copy file or directory or content of directory,  we can copy multiple files at the same time but the destination should be directory in this case,
	8- rm -->> to remove file or directory with option (-d), but if user is root it is interactive by default before removing it asks, to disable interactive we can use option (-f  --> force), to delete non empty directory we use option (-r).

9- nautilus -->> to open file explorer (GUI file explorer).

10- echo -->> to print something in terminal.

As I have said before Linux is hierarchal or tree system:
	1- / -->> root or top directory which holds all Linux files.

2- /boot -->> files to start boot process.

3- /dev -->> special devices files to access hardware.

4- /etc -->> system configuration files.

5- /home -->> home directory for normal users where they store their data and config files.

6- /root -->> home directory for super user or root.

7- /run -->> run time data for process that started from last boot process.

8- /tmp -->> world writable (any user can access) space for temporary files, the ignored files for 10 days are deleted by default.

9- /usr  -->> contains user-installed software, libraries, and documentation shared across the system.

10- /lib -->> contains essential shared libraries and kernel modules needed to boot.

11- /bin -->> contains  user commands binaries.

12- /sbin -->> contains root only commands binaries.

13- /var -->> stores variable data that changes during system run time like logs, /var/tmp is for temporary files also but if they are ignored for 30 days they are deleted by default.

