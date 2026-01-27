# Navigation actions

<a id="GoToGithub"></a>

## ![Go to GitHub icon](images/GoToGithub-icon.png) Go to GitHub

For the github file system, go to the GitHub website of the current directory

![Go to GitHub screenshot](images/GoToGithub-screenshot.png)

<a id="GoTo"></a>

## ![Go To... icon](images/GoTo-icon.png) Go To...

Open a window to select a new location for the current panel

Shortcut: <kbd>Ctrl</kbd> + <kbd>G</kbd> (<kbd>⌘</kbd> + <kbd>G</kbd>)

![Go To... screenshot](images/GoTo-screenshot.png)

<a id="GoToClusterFile"></a>

## ![Show files from all cluster icon](images/GoToClusterFile-icon.png) Show files from all cluster

Open a cluster file in a cluster file system

<a id="GoToLink"></a>

## ![Go to Link icon](images/GoToLink-icon.png) Go to Link

Go to the location that the link is pointing to

<a id="SuperBookmark1"></a>

## ![Super Bookmark 1 icon](images/SuperBookmark1-icon.png) Super Bookmark 1

Go to the location of the super bookmark n°1

Shortcut: <kbd>Ctrl</kbd> + <kbd>1</kbd> (<kbd>⌘</kbd> + <kbd>1</kbd>)

<a id="SuperBookmark2"></a>

## ![Super Bookmark 2 icon](images/SuperBookmark2-icon.png) Super Bookmark 2

Go to the location of the super bookmark n°2

Shortcut: <kbd>Ctrl</kbd> + <kbd>2</kbd> (<kbd>⌘</kbd> + <kbd>2</kbd>)

<a id="SuperBookmark3"></a>

## ![Super Bookmark 3 icon](images/SuperBookmark3-icon.png) Super Bookmark 3

Go to the location of the super bookmark n°3

Shortcut: <kbd>Ctrl</kbd> + <kbd>3</kbd> (<kbd>⌘</kbd> + <kbd>3</kbd>)

<a id="Forward"></a>

## ![Forward icon](images/Forward-icon.png) Forward

Go to the next file or directory from the history

<a id="Reload"></a>

## ![Reload icon](images/Reload-icon.png) Reload

Reload the current location

<a id="OpenAsZip"></a>

## ![Open file as zip file icon](images/OpenAsZip-icon.png) Open file as zip file

Open the selected file as a directory by considering that it's a zip file

<a id="ShowTopUsedSetLocation"></a>

## ![Show Top Used Locations icon](images/ShowTopUsedSetLocation-icon.png) Show Top Used Locations

Show a window with the top visited locations

![Show Top Used Locations screenshot](images/ShowTopUsedSetLocation-screenshot.png)

<a id="LazyReload"></a>

## ![Lazy Reload icon](images/LazyReload-icon.png) Lazy Reload

Reload the file or directory without updating the current panel if the file or directory hasn't changed

<a id="OtherPanel"></a>

## ![Other Panel icon](images/OtherPanel-icon.png) Other Panel

Navigate to the same location than the panel next to it

<a id="Home"></a>

## ![Home icon](images/Home-icon.png) Home

Go to the user home directory

<a id="Up"></a>

## ![Up icon](images/Up-icon.png) Up

Go to the parent directory of the current location

Shortcut: <kbd>Alt</kbd> + <kbd>UP</kbd> (<kbd>⌥</kbd> + <kbd>UP</kbd>)

<a id="AddPlugInBookmark"></a>

## ![Add Bookmark icon](images/AddPlugInBookmark-icon.png) Add Bookmark

Add the current location to the bookmarks of the panel type

<a id="GoToCluster"></a>

## ![Go to Cluster icon](images/GoToCluster-icon.png) Go to Cluster

Create/Open a cluster file system

![Go to Cluster screenshot](images/GoToCluster-screenshot.png)

<a id="NextDirFile"></a>

## ![Next icon](images/NextDirFile-icon.png) Next

Open the next file in the same directory

<a id="AddBookmark"></a>

## ![Add Bookmark icon](images/AddBookmark-icon.png) Add Bookmark

Add a bookmark

Shortcut: <kbd>Ctrl</kbd> + <kbd>B</kbd> (<kbd>⌘</kbd> + <kbd>B</kbd>)

<a id="PlugInBookmark"></a>

## ![Bookmarks icon](images/PlugInBookmark-icon.png) Bookmarks

List the bookmark of the panel type

<a id="Roots"></a>

## ![Choose Disk icon](images/Roots-icon.png) Choose Disk

Show the possible local file roots to navigate to

![Choose Disk screenshot](images/Roots-screenshot.png)

<a id="Selection"></a>

## ![Go To Selected File icon](images/Selection-icon.png) Go To Selected File

Go to the selected file

<a id="GoToLocal"></a>

## ![Open local file icon](images/GoToLocal-icon.png) Open local file

Open a local file chooser

<a id="PasteLocation"></a>

## ![Go To Clipboard Content icon](images/PasteLocation-icon.png) Go To Clipboard Content

Go to the location that is in the clipboard

<a id="ChangeLocation"></a>

## ![Change Location icon](images/ChangeLocation-icon.png) Change Location

Change the panel location of the target panel to match the source panel

<a id="GoToTextField"></a>

## ![Go to text field icon](images/GoToTextField-icon.png) Go to text field

Open a window that allows you to enter the url of the location you want to go to

![Go to text field screenshot](images/GoToTextField-screenshot.png)

Ant Commander Pro supports special macros for some directories (e.g. &lt;home&gt;\Documents):
* &lt;home&gt; or ~ : User home directory
* &lt;temp&gt; : User temporary directory
* &lt;root&gt; : Root of the user directory
* &lt;clipboard&gt; : The content of the clipboard
* &lt;Env.*&gt; : A directory specified in an environment variable (e.g. &lt;Env.windir&gt;\system32)
* &lt;Now.pattern&gt; : Replace pattern with the current date (e.g. &lt;home&gt;\Documents\Reports_&lt;Now.YYYY-MM-dd&gt;)
* <antcommander.data> : The Ant Commander data directory
* <antcommander.app> : The Ant Commander application directory
* <antcommander.jar> : The location of the AntCommander.jar
* <super.bookmark1> (2,3) : The location specified in the super bookmark 1 (2,3)
* <selected.file> : The currently selected file (or 1st file selected if multiple)
* <selected.file.x> : The x currently selected file when multiple are selected
* <current.location> : The currently selected panel location
* <Win.key> : The Windows shell folder defined by key in HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Shell Folders in the registry (e.g. <Win.My Pictures>)
* <default> : The OS default directory (e.g. <home>\Documents on Windows)
* <"HK..."> : The directory or file defined in the Windows registry (e.g. <"HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Shell Folders" /v "Local AppData">

<a id="Back"></a>

## ![Back icon](images/Back-icon.png) Back

Go to the previous file or directory from the history

<a id="Root"></a>

## ![Root icon](images/Root-icon.png) Root

Go to the root location to the current file system

<a id="PreviousDirFile"></a>

## ![Previous icon](images/PreviousDirFile-icon.png) Previous

Open the previous file in the same directory

<a id="CloseConnection"></a>

## ![Close connection icon](images/CloseConnection-icon.png) Close connection

Close the network connection for network file systems

<a id="ShowPopUpPlugInBookmarks"></a>

## ![Bookmarks icon](images/ShowPopUpPlugInBookmarks-icon.png) Bookmarks

List the bookmark of the panel type in a pop-up menu

<a id="GoToMatching"></a>

## ![Go to Matching icon](images/GoToMatching-icon.png) Go to Matching

If a file system can have a matching file (like .lst), go to the matching file

<a id="Bookmark"></a>

## ![Bookmarks icon](images/Bookmark-icon.png) Bookmarks

List the application bookmarks

