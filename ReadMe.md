A Xcode project that builds [VDrift's][1] required dependancies as native OS X
frameworks. For instructions about VDrift itself visit the [wiki][2]. Released
under the [GNU General Public License (GPL) v3][3].

If you know a better way of doing any part of this, or find a bug, please make
an issue or send a pull request on [GitHub][4].

# Prerequisites
To build these frameworks you need Xcode 3.2 or later (tested only with Xcode
6.1). Xcode is available free on the [Mac App Store][5].

# Downloads
Once you have the prerequisites, download the latest stable release from the
following sites. You don't need all of them, but some require one or more of the
others. Make sure you download the source releases, not the packaged or binary
versions.

Bullet: [http://bulletphysics.org/][6]

cURL: [http://curl.haxx.se][7]

Ogg: [http://xiph.org/downloads/][8]

SDL2: [http://libsdl.org/index.php][9]

SDL2_image (**Requires SDL2 and WebP**): [http://libsdl.org/projects/SDL_image/][10]

Vorbis (**Requires Ogg**): [http://xiph.org/downloads/][8]

WebP: [https://developers.google.com/speed/webp/][11]

Next expand the downloaded file into the relevant folder, removing the version
number from the resultant folder, for example expand _libogg-1.3.0.tar.gz_ into
_vdrift-frameworks/Ogg/libogg/_

# Updating
Update the version in _vdrift-frameworks/**FRAMEWORK**/**FRAMEWORK**-Info.plist_
and the _Compatibility Version_, _Current Library Version_ and
_Framework Version_ in the appropriate build settings in Xcode according to
[Apple's documentation][12].

# Building
You can now open _vdrift-frameworks/vdrift-frameworks.xcodeproj_ and build some
or all of the frameworks - use the drop down on the toolbar to select the
required scheme. They will be put into your build directory from which you can
copy them into _vdrift/vdrift-mac/Frameworks/_.

# No longer supported
VDrift no longer depends on these libraries, so this project is no longer
updated for new versions. The targets have been left in case they are useful for
someone, but they may break at anytime.

Archive: [http://libarchive.org][13]

GLEW: [http://glew.sourceforge.net/][14]

SDL: [http://libsdl.org/download-1.2.php][15]

SDL_gfx (**Requires SDL**):
[http://ferzkopp.net/joomla/software-mainmenu-14/4-ferzkopps-linux-software/19-sdlgfx][16]

SDL_image (**Requires SDL**): [http://libsdl.org/projects/SDL_image/release-1.2.html][17]

SDL_net (**Requires SDL**): [http://libsdl.org/projects/SDL_net/release-1.2.html][18]

SDL2_gfx (**Reqires SDL2**): [http://ferzkopp.net/joomla/software-mainmenu-14/4-ferzkopps-linux-software/19-sdlgfx][16]

[1]: http://vdrift.net
[2]: http://wiki.vdrift.net
[3]: http://gnu.org/copyleft/gpl.html
[4]: http://github.com/Timo6/vdrift-frameworks
[5]: http://itunes.apple.com/us/app/xcode/id422352214?mt=12&ls=1
[6]: http://bulletphysics.org/wordpress/
[7]: http://curl.haxx.se
[8]: http://xiph.org/downloads/
[9]: http://libsdl.org/index.php
[10]: http://libsdl.org/projects/SDL_image/
[11]: https://developers.google.com/speed/webp/
[12]: http://developer.apple.com/library/mac/#documentation/MacOSX/Conceptual/BPFrameworks/Concepts/VersionInformation.html
[13]: http://libarchive.org
[14]: http://glew.sourceforge.net/
[15]: http://libsdl.org/download-1.2.php
[16]: http://ferzkopp.net/joomla/software-mainmenu-14/4-ferzkopps-linux-software/19-sdlgfx
[17]: http://libsdl.org/projects/SDL_image/release-1.2.html
[18]: http://libsdl.org/projects/SDL_net/release-1.2.html

vdrift-frameworks.xcodeproj was created by Timothy Furlong.
