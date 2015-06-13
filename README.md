This repository contains a fork of [7-zip](http://www.7-zip.org) used in [FileArchiver](https://github.com/Strachu/FileArchiver).

The original 7-zip application has been modified to enable access to accurate progress of pending operations for
applications invoking the command line version of 7-zip (7zr.exe). For more details about the changes see
[the commit log](https://github.com/Strachu/7-zip/commits/master).

#How to compile
Follow the instructions at http://www.ski-epic.com/2012_compiling_7zip_on_windows_with_visual_studio_10/index.html.  
In short:

1. Install Microsoft Visual Studio (these steps were tested with Visual Studio 2013)
2. Open command line
3. Execute the following commands (but first substitute the values in {} for correct path):
```
cd "{path_to_visual_studio}\Common7\Tools"
vsvars32.bat
cd "{path_to_directory_with_this_file}\CPP\7zip\Bundles\Alone7z"
nmake NEW_COMPILER=1 MY_STATIC_LINK=1
```

The resulting file is at {path_to_directory_with_this_file}\CPP\7zip\Bundles\Alone7z\O\7zr.exe
