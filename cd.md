The cd Command

The cd command is used to change the current directory (i.e., the directory in which the user is currently working) in Linux and other Unix-like operating systems. It is similar to the CD and CHDIR commands in MS-DOS.

cd's syntax is

    cd [option] [directory]

The items in square brackets are optional. When used without specifying any directory name, cd returns the user to the previous current directory. This provides a convenient means of toggling between two directories.

When a directory name is provided, cd changes the current directory to it. The name can be expressed as an absolute pathname (i.e., location relative to the root directory) or as a local pathname (i.e., location relative to the current directory). It is usually more convenient to use a local pathname when changing to a subdirectory of the current directory.

As an example, the following would change the current directory, regardless of where it is on the system (because it is an absolute path), to the root directory (which is represented by a forward slash):

    cd /

Likewise, the following would change the current directory, regardless of its location, to the /usr/sbin directory (which contains non-vital system utilities that are used by the system administrator):

    cd /usr/sbin

If a user currently in the directory /usr/local/share/man/ desired to change to the directory /usr/local/share/man/man2, which is a subdirectory of the current directory, it would be possible to change by using the absolute pathname, i.e.,

    cd /usr/local/share/man/man2

However, it would clearly be much less tedious to use the relative pathname, i.e.,

    cd man2

On Unix-like operating systems the current directory is represented by a single dot and its parent directory (i.e., the directory that contains it) is represented by two consecutive dots. Thus, it is possible (and often convenient) to change to the parent of the current directory by using the following:

    cd ..

Another convenient feature of cd is the ability for any user to return directly to its home directory by merely using a tilde as the argument. A home directory, also called a login directory, is the directory on a Unix-like operating system that serves as the repository for a user's personal files, directories and programs. It is also the directory that a user is first in after logging into the system. A tilde is a short, wavy, horizontal line character that represents the home directory of the current user. That is, any user can return immediately to its home directory by typing the following and then pressing the Enter key:

    cd ~

This is easier than typing the full name of the user's home directory, for instance, /home/josephine in the case of a user named josephine. (And it is just one of the numerous shortcuts that help make the command line on Unix-like operating systems so easy to use.)

When followed by a space and then a hyphen, cd both returns the user to the previous current directory and reports on a new line the absolute pathname of that directory. This can further enhance the already convenient toggling capability of cd. Toggling is particularly convenient when at least one of the two directories has a long absolute pathname, such as /usr/local/share/man/man2.

cd has only two options, and neither of them are commonly used. The -P option instructs cd to use the physical directory structure instead of following symbolic links. The -L option forces symbolic links to be followed. 


Created May 25, 2006. Updated August 11, 2007.
Copyright © 2006 - 2007. The Linux Information Project. All Rights Reserved.
