# Bash Command Line Tutorials

## The Command Line

- command line: is a text based interface to the system and You are able to enter commands by typing them on the keyboard and will be given you feedback as text.

- how does it work:

1. presents us with a prompt, After that we entered a command .
2. then you will see output from running the command.
3. presents us with a prompt again.

- Opening a terminal:

1. find the program Terminal under Applications -> Utilities.
2. click 'command + space' then start typing Terminal and it will soon show up.

## Basic Navigation

pwd: Print Working Directory (Where are we currently).
ls: List the contents of a directory.
cd: Change Directories - ie. move to another directory.

## More About Files

In other systems such as Windows the extension is important and the system uses it to determine what type of file it is. Under Linux the system actually ignores the extension and looks inside the file to determine what type of file it is. As such it can sometimes be hard to know for certain what type of file a particular file is. Luckily there is a command called file which we can use to find this out.

## Manual Pages

The manual pages are a set of pages that explain every command available on your system including what they do, the specifics of how you run them and what command line arguments they accept.

- man command: Look up the manual page for a particular command.
- man -k search term: Do a keyword search for all manual pages containing the given search term.
- /term: Within a manual page, perform a search for 'term'
- n: After performing a search within a manual page, select the next found item.

## File Manipulation

- mkdir: Make Directory - ie. Create a directory.
- rmdir: Remove Directory - ie. Delete a directory.
- touch: Create a blank file.
- cp: Copy - ie. Copy a file or directory.
- mv: Move - ie. Move a file or directory (can also be used to rename).
- rm: Remove - ie. Delete a file.
