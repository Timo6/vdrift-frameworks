A Xcode project that builds the dependancies [VDrift](http://vdrift.net)
requires as native Mac OS X frameworks. For instructions about VDrift itself
visit the [wiki](http://wiki.vdrift.net). Released under the
[GNU General Public License (GPL) v3](http://gnu.org/copyleft/gpl.html).

If you know a better way of doing any part of this, or find a bug, please make
an issue or send a pull request on [GitHub](http://github.com/Timo6/vdrift-frameworks).

# Prerequisites
To build these frameworks you need Xcode 3.2 or later (tested only with Xcode
4.2 to 4.3.2). Xcode is available free on the
[Mac App Store](http://itunes.apple.com/us/app/xcode/id422352214?mt=12&ls=1).

You also need [CMake](http://cmake.org/cmake/resources/software.html). You can
either use the GUI or, as in the following instructions, the command line tools.
Just make sure you select _Install Command Line Links_ when asked at the end of
the install.

# Downloads
Once you have the prerequisites, download the latest stable release from the
following sites. You don't need all of them, but some require one of more of the
others. Make sure you download the source releases, not the packaged or binary
versions.

Archive:
[http://libarchive.github.com/](http://libarchive.github.com/)

BulletCollision (**Requires LinearMath**):
[http://code.google.com/p/bullet/downloads/list](http://code.google.com/p/bullet/downloads/list)

BulletDynamics (**Requires LinearMath and BulletCollision**):
[http://code.google.com/p/bullet/downloads/list](http://code.google.com/p/bullet/downloads/list)

BulletSoftBody (**Requires LinearMath, BulletCollision and BulletDynamics**):
[http://code.google.com/p/bullet/downloads/list](http://code.google.com/p/bullet/downloads/list)

cURL:
[http://curl.haxx.se/download.html](http://curl.haxx.se/download.html)

GLEW:
[http://glew.sourceforge.net/](http://glew.sourceforge.net/)

LinearMath:
[http://code.google.com/p/bullet/downloads/list](http://code.google.com/p/bullet/downloads/list)

Ogg:
[http://xiph.org/downloads/](http://xiph.org/downloads/)

SDL:
[http://libsdl.org/download.php](http://libsdl.org/download.php)

SDL_gfx (**Requires SDL**):
[http://ferzkopp.net/joomla/software-mainmenu-14/4-ferzkopps-linux-software/19-sdlgfx](http://ferzkopp.net/joomla/software-mainmenu-14/4-ferzkopps-linux-software/19-sdlgfx)

SDL_image (**Requires SDL**):
[http://libsdl.org/projects/SDL_image/](http://libsdl.org/projects/SDL_image/)

SDL_net (**Requires SDL**):
[http://libsdl.org/projects/SDL_net/](http://libsdl.org/projects/SDL_net/)

Vorbis (**Requires Ogg**):
[http://xiph.org/downloads/](http://xiph.org/downloads/)

Next expand the downloaded file into the relevant folder, removing the version
number from the resultant folder, for example expand _libogg-1.3.0.tar.gz_ into
_vdrift-frameworks/Ogg/libogg/_

# Configuring
Now you need to configure a few of the libraries before we can build the
frameworks.

## Archive
In a command line:

    cd vdrift-frameworks/Archive/libarchive
    ./configure

Open _vdrift-frameworks/Archive/libarchive/config.h_ and change the number at
the end of line 607

    #define HAVE_STRUCT_STAT_ST_BIRTHTIME

and line 610

    #define HAVE_STRUCT_STAT_ST_BIRTHTIMESPEC_TV_NSEC

from 1 to 0.

## cURL
    cd vdrift-frameworks/cURL/curl
    mkdir xcode
    cd xcode
    cmake -G "Xcode" ../

## All
Update the version in _vdrift-frameworks/**FRAMEWORK_NAME**/**FRAMEWORK_NAME**-Info.plist_
and the _Compatibility Version_, _Current Library Version_ and _Framework Version_
in the appropriate build settings in Xcode according to
[Apple's documentation][1].

# Building
You can now open _vdrift-frameworks/vdrift-frameworks.xcodeproj_ and build some
or all of the frameworks - use the drop down on the toolbar to select the
required scheme. They will be put into _vdrift-frameworks/build/Debug/_ from which
you can copy them into _vdrift/vdrift-mac/Frameworks/_

[1]: http://developer.apple.com/library/mac/#documentation/MacOSX/Conceptual/BPFrameworks/Concepts/VersionInformation.html.



vdrift-frameworks.xcodeproj was created by Timothy Furlong.
