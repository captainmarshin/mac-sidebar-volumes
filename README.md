# mac-sidebar-volumes

**[mysides](https://github.com/mosen/mysides)** tool allows you to list, add, and remove items in Finder's sidebar. The original script works only with the Favorites category. In this version, I simply changed the Favorites category to the Locations category, which allows you to list, add, and remove items in the Locations category.

No code was changed except for the list name. All functions and code structure remained the same.

## How to use
You can open this repo in Xcode and build it, after navigating to the Build folder, copy **mysides** path to Terminal and run it. Or, you can download the built executable from the [Releases](https://github.com/captainmarshin/mac-sidebar-volumes/releases) page.

## Commands

List sidebar Locations items:

    path/to/mysides list

Append a new item to the end of a list:

    path/to/mysides add example file:///Users/Shared/example

Insert a new item at the start of the list:

    path/to/mysides insert example file:///Users/Shared/example

Remove the item (by name):

    path/to/mysides remove example

<hr>

All credits to [mosen](https://github.com/mosen) for this incredible tool.

<details>
    <summary>Original README</summary>
    
## mysides ##

A simple CLI tool for Finder sidebar modification.

**NOTE**: I clobbered this together with very little experience in C/CoreFoundation, as a result the code may be horrible.

**NOTE*: Using Versions 10.11 El Capitan or 10.12 Sierra, you can also use `sfltool` to achieve similar things. _These options were removed in 10.13 High Sierra onwards [*][1013-regression]._ Example:

    $ sfltool add-item com.apple.LSSharedFileList.FavoriteItems file:///Path/To/Sidebar/Folder

## Usage ##

List sidebar favorites items:

    mysides list

Append a new item to the end of a list:

    mysides add example file:///Users/Shared/example

Insert a new item at the start of the list:

    mysides insert example file:///Users/Shared/example

Remove the item (by name):

    mysides remove example

## Credits ##

portions (l) copyleft 2011 Adam Strzelecki nanoant.com
without whom I would not know much about the LSSharedFileList API.

 [1013-regression]: https://openradar.appspot.com/radar?id=4985135170584576

</details>
