QLNetcdf
========
A QuickLook Plugin for previewing 
[NetCDF](http://www.unidata.ucar.edu/software/netcdf/) files. When a NetCDF file is selected in macOS Finder and the spacebar is pressed, the QuickLook feature is activated.  With this plugin installed, along with `ncdump`, the contents of a NetCDF file can be shown in the QuickLook window.  This plugin runs `ncdump` with the `-h` option to print header information only (no data) and `-s` to print special attributes (i.e. compression values, chunksizes, etc).

Requires that `ncdump` is installed at `/usr/local/bin`

Fortunately if you installed `netcdf` using [Homebrew](http://brew.sh) (with 
the default settings) then `ncdump` should exist in the correct location 
already.

Example
-------
Here is an example.

![Screen shot](/images/example0.png?raw=true "QLNetcdf generator in action")

Installing
-----------
Download one of the releases and copy the QLNetcdf.qlgenerator file to your 
`~/Library/QuickLook/` directory (or `/Library/QuickLook/` to make the plugin 
available to all users).

You may have to force the QuickLook Server to reload so it picks up the new 
generator:

    $ qlmnange -r

Known Issues
------------
Sometimes the plugin fails to work (no preview is rendered). The best fix I have found is to force-relaunch Finder (`cmd+option+esc`)

Building
--------
The Xcode project file is supplied with the project. The project has been built with Xcode versions 4.6 and 5.1.
