A Xcode project that builds the dependancies [VDrift][1] requires as native OS X
frameworks. For instructions about VDrift itself visit the [wiki][2]. Released
under the [GNU General Public License (GPL) v3][3].

If you know a better way of doing any part of this, or find a bug, please make
an issue or send a pull request on [GitHub][4].

# Prerequisites
To build these frameworks you need Xcode 3.2 or later (tested only with Xcode
4.2 to 4.5). Xcode is available free on the [Mac App Store][5].

In order to build cURL you also need [CMake][6] installed. If using the package
from the website, make sure you select 'Install Command Line Links' when asked
at the end of the install.

# Downloads
Once you have the prerequisites, download the latest stable release from the
following sites. You don't need all of them, but some require one or more of the
others. Make sure you download the source releases, not the packaged or binary
versions.

Archive: [http://libarchive.github.com/][7]

BulletCollision (**Requires LinearMath**):
[http://code.google.com/p/bullet/downloads/list][8]

BulletDynamics (**Requires LinearMath and BulletCollision**):
[http://code.google.com/p/bullet/downloads/list][8]

BulletSoftBody (**Requires LinearMath, BulletCollision and BulletDynamics**):
[http://code.google.com/p/bullet/downloads/list][8]

cURL: [http://curl.haxx.se/download.html][9]

GLEW: [http://glew.sourceforge.net/][10]

LinearMath: [http://code.google.com/p/bullet/downloads/list][8]

Ogg: [http://xiph.org/downloads/][11]

SDL: [http://libsdl.org/download.php][12]

SDL_gfx (**Requires SDL**):
[http://ferzkopp.net/joomla/software-mainmenu-14/4-ferzkopps-linux-software/19-sdlgfx][13]

SDL_image (**Requires SDL**): [http://libsdl.org/projects/SDL_image/][14]

SDL_net (**Requires SDL**): [http://libsdl.org/projects/SDL_net/][15]

Vorbis (**Requires Ogg**): [http://xiph.org/downloads/][16]

Next expand the downloaded file into the relevant folder, removing the version
number from the resultant folder, for example expand _libogg-1.3.0.tar.gz_ into
_vdrift-frameworks/Ogg/libogg/_

# Updating
Update the version in _vdrift-frameworks/**FRAMEWORK**/**FRAMEWORK**-Info.plist_
and the _Compatibility Version_, _Current Library Version_ and
_Framework Version_ in the appropriate build settings in Xcode according to
[Apple's documentation][17].

# Building
You can now open _vdrift-frameworks/vdrift-frameworks.xcodeproj_ and build some
or all of the frameworks - use the drop down on the toolbar to select the
required scheme. They will be put into your build directory from which you can
copy them into _vdrift/vdrift-mac/Frameworks/_.

[1]: http://vdrift.net
[2]: http://wiki.vdrift.net
[3]: http://gnu.org/copyleft/gpl.html
[4]: http://github.com/Timo6/vdrift-frameworks
[5]: http://itunes.apple.com/us/app/xcode/id422352214?mt=12&ls=1
[6]: http://cmake.org/cmake/resources/software.html
[7]: http://libarchive.github.com/
[8]: http://code.google.com/p/bullet/downloads/list
[9]: http://curl.haxx.se/download.html
[10]: http://glew.sourceforge.net/
[11]: http://xiph.org/downloads/
[12]: http://libsdl.org/download.php
[13]: http://ferzkopp.net/joomla/software-mainmenu-14/4-ferzkopps-linux-software/19-sdlgfx
[14]: http://libsdl.org/projects/SDL_image/
[15]: http://libsdl.org/projects/SDL_net/
[16]: http://xiph.org/downloads/
[17]: http://developer.apple.com/library/mac/#documentation/MacOSX/Conceptual/BPFrameworks/Concepts/VersionInformation.html.



vdrift-frameworks.xcodeproj was created by Timothy Furlong.
