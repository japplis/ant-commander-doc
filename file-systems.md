# File Systems

## Local

Local files includes
* Hard disks
* USB sticks
* Mounted directories
* Mounted Network Drives
* Shared drives/UNC Paths
* WSL (Windows Subsystem for Linux) drive
* Docker client drive
* Google Drive <sup>1</sup>
* OneDrive <sup>1</sup>
* Dropbox <sup>1</sup>

_<sup>1</sup> The drive client application needs to be running to synchronize the files with the server_

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

Network files are not available in the free version of Ant Commander.

The following network file systems are currently supported:
* ftp
* sftp
* ftps
* WebDAV(s)
* http(s)
* NFS nfs3://[username[:password]@]hostname[:port]/[export-path]/[absolute-path]
* Samba/CIFS smb://[username[:password]@]hostname[:port][absolute-path]
* Samba2 (smb2://)

Use the _Navigation -> Go To..._ action to go to a network directory.

Note that you can bookmark it afterwards.

## Rclone

[Rclone](https://rclone.org/) is a free software to manager files on cloud storage. 
It supports more than [70 cloud storage products](https://rclone.org/#providers) including Amazon AWS S3, Microsoft Azure Blob and Files Storage, Minio, 
Google Cloud Storage, Google Drive, Dropbox, Box, Blackblaze B2, Cloudflare R2, DigitalOcean Spaces and iCLoud Drive. 

You will first need to install Rclone on your computer. Rclone is available for Windows, MacOS and Linux.

If Rclone is not defined in the PATH environment variable, provide in the _File system settings_ the path to the executable.

When _Rclone_ create a remote config, using [rclone config](https://rclone.org/#providers). Once the config create, you can access it using _rclone://remote-name/path_. For example: rclone://my-gdrive/backups/data.zip

Ant Commander Pro handles no authentication credentials. It relies entirely on the environment having a valid `rclone.conf`.

To access a rclone file system, use _Navigation -> File Systems -> Go to Rclone_, select the remote and the path.
The path can be empty for the root and should not start with /. Click on the + button to add or manage remotes.

`rclone listremotes` can be used to list the remote names already configured.

## Cloud (experimental)

Work has been done in Ant Commander Pro to also have access to cloud file systems without using Rclone. 
This work is still experimental and is not included in Ant Commander Pro due to the important files size for the libraries,
the beta state of the code and lack of possibility to test it in a real enterprise environment.

If you are interested to use any of these file systems at your company, contact [info@japplis.com](mailto:info@japplis.com) to apply for the beta testing phase.

The following cloud file systems are in experimental phases and **not available by default**:
* Amazon S3
* Microsoft Azure Storage
* Google Storage
* Google Drive
* Dropbox

### Amazon S3 (experimental)

The S3 file system is not only used at Amazon AWS but also at companies like Backblaze, Wasabi, Exoscale, OVH Cloud, IBM Cloud storage and more.

For Amazon S3, use _F9 -> Go to S3_

Another way is using _Go to S3 provider_

* Access key and secret key can be provided in the form or via an _credentials_ file
* Session token is optional

For more details, see [Amazon credentials documentation](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/credentials.html)

S3 urls are s3://. Note that s3a:// and s3n:// may be supported (not tested)

### Azure (experimental)

For Microsoft Azure Storage, use _F9 -> Go to Azure_

* The key consist of a long set of characters and numbers
* The endpoint is optional and will default to https://"account_name".dfs.core.windows.net

Azure url is azure:// or azfs://

### Dropbox (experimental)

For Dropbox, use _F9 -> Go to Dropbox_

You will need a OAuth token, see 
[Dropbox documentation](https://developers.dropbox.com/nl-nl/oauth-guide#testing-with-a-generated-token) for more details.

Dropbox url is dropbox://

### Google Storage (experimental)

For Google Storage, use _F9 -> Go to Google Storage_

You can provide either a _Service account key file_ or a _storage key_

Google Storage url is gs://

### Google Drive (experimental)

For Google Drive, use _F9 -> Go to Google Drive_

You will need a crednetials file, see [Google documentation](https://developers.google.com/workspace/drive/api/quickstart/java#authorize_credentials_for_a_desktop_application) on how to get it.

You will other need a token. Ant Commander Pro will open the browser for you to authenticate and save the token in the designated token directory.

Google Drive url is googledrive://

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