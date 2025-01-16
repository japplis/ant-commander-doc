# File Systems

## Local

Local files includes
* Hard disks
* USB sticks
* Mounted directories
* Mounted Network Drives
* Shared drives/UNC Paths

Here are a few example of local files:
* C:\Temp\Test
* /usr/bin/bash.txt
* \\\\wsl.localhost\Ubuntu\tmp
* file:///C:/Ima/Decoration/license.txt

## Compressed

Compressed file system are read only file systems.
You cannot modify the content of the compressed files and directories.

Ant Commander Pro will handle the compressed files like a directory provided that the file name uses a standard extension.
This means that double clicking it or alt + click or Enter key will navigate inside the compressed file.

To execute a compressed file, select the file and click on the `Execute` button in the status bar.

To open a Zip file with another extension than 'zip', select the file, use F9 and 'Open file as zip file' action.

The following compression formats are currently supported:
* Zip
* Jar (ear/war)
* Tar
* Gzip (gz)
* Bzip2
* Z
* XZ
* LZ4

Here are a few examples of url:
* jar:file:///C:/Ima/Decoration/Decoration.jar!/
* tar:xz:file:///C:/Temp/4.5/bla.tar.xz!/bla.tar!/test1.xml
* tgz:file:///C:/Java/japplis/control-dashboard/ControlDashboard.tgz!/ControlDashboard

## Network

The following network file systems are currently supported:
* ftp
* sftp
* ftps
* WebDAV(s)
* http(s)
* NFS nfs3://[username[:password]@]hostname[:port]/[export-path]/[absolute-path]
* Samba/CIFS smb://[username[:password]@]hostname[:port][absolute-path]
* Samba2 (smb2://)
* Amazon S3

Use the _Navigation -> Go To..._ action to go to a network directory.

For Amazon S3, use _F9 -> Go to S3_

Note that you can bookmark it afterwards.

## Other

### Lst

Lst files are text files containing list of files with size and last modified date.

Use _F9 -> Store directory files in text_ to create a lst file of a directory.

To open it, just double click on the created .lst file.

This file system is read only and cannot view file content unless the listed directory is still accessible.

It is possible to match a .lst file with a directory with _F9 -> Match Lst with Directory_, for example to quickly search files and still be able to open files.

### GitHub

The github file system allows to browse a remote github repository in Ant Commander Pro like a file system.

Use _F9 -> Go to GitHub_ action to open this file system

I highly advise in creating an API Token key to be able to do more requests to the GitHub API.

The URL should look like https://github.com/organization/project-name/tree/branch-name

The GitHub file system is read-only.

### Cluster

The cluster file system allow to view multiple similar directories as one.

Use the [Go to cluster](files.md#GoToCluster) action to enter the list of directories.

If a file is not in all directories, the file name will look more transparent.

The size and date of the last modified file is used in the directory table panel.

Clicking on a file will show the files (with the same name) in the different directories. The tooltip will show you the absolute path of the file.
Note that technically this is another file system.

### Bookmark

The bookmark file system will show the bookmark like if it was a directory. Clicking on a bookmark (file or directory) will open the file or directory.

Use _Navigation -> Go To... -> Drives drop down_ to go to a bookmark file system.

### Bookmark file

The bookmark file file system is a file system that takes a text file (.bookmarks extension) as input and create a file system based on the bookmarks in text file.

Like for Lst or compressed file, just double click on the .bookmarks text file to open the file system.

You can manipulate the bookmarks in this file system by copying files, moving files, renaming files, creating folders.

This file system is in beta stage, so you may experience more bugs. In this case, you can always edit the .bookmarks file using a text editor.

### RAM

Ram will store files and directories in the RAM of the computer.

Note that as soon as you close the application, all files and directories in this file system will be permanently deleted.

## URL
File locations are stored with URLs. More info at the [Commons VFS website](https://commons.apache.org/proper/commons-vfs/filesystems.html)