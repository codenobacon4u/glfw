# GLFW

## Introduction

GLFW is a free, Open Source, multi-platform library for OpenGL and OpenGL ES
application development.  It provides a simple, platform-independent API for
creating windows and contexts, reading input, handling events, etc.

Version 3.2 is _not yet described_.

If you are new to GLFW, you may find the
[introductory tutorial](http://www.glfw.org/docs/latest/quick.html) for GLFW
3 useful.  If you have used GLFW 2 in the past, there is a
[transition guide](http://www.glfw.org/docs/latest/moving.html) for moving to
the GLFW 3 API.


## Compiling GLFW

See the [Compiling GLFW](http://www.glfw.org/docs/latest/compile.html) guide in
the GLFW documentation.


## Using GLFW

See the
[Building programs that use GLFW](http://www.glfw.org/docs/latest/build.html)
guide in the GLFW documentation.


## Reporting bugs

Bugs are reported to our [issue tracker](https://github.com/glfw/glfw/issues).
Please always include the name and version of the OS where the bug occurs and
the version of GLFW used.  If you have cloned it, include the commit ID used.

If it's a build issue, please also include the build log and the name and
version of your development environment.

If it's a context creation issue, please also include the make and model of your
graphics card and the version of your driver.

This will help both us and other people experiencing the same bug.


## Dependencies

GLFW itself needs only the headers and libraries for your window system.  It
does not need the headers for any context creation API (WGL, GLX, EGL, NSGL) or
client API (OpenGL, OpenGL ES) to enable support for them.

GLFW bundles a number of dependencies in the `deps/` directory.  These are only
used by the tests and examples and are not required to build the library.

 - [getopt\_port](https://github.com/kimgr/getopt_port/) for examples
   with command-line options
 - [TinyCThread](https://github.com/tinycthread/tinycthread) for threaded
   examples
 - An OpenGL 3.2 core loader generated by
   [glad](https://github.com/Dav1dde/glad) for examples using modern OpenGL
 - [linmath.h](https://github.com/datenwolf/linmath.h) for linear algebra in
   examples


## Changelog

 - Added `glfwSetWindowSizeLimits` and `glfwSetWindowAspectRatio` for setting
   absolute and relative window size limits
 - Added `glfwGetKeyName` for querying the layout-specific name of printable
   keys
 - Added `GLFW_NO_API` for creating window without contexts
 - Added `GLFW_CONTEXT_NO_ERROR` context hint for `GL_KHR_no_error` support
 - Added `GLFW_TRUE` and `GLFW_FALSE` as client API independent boolean values
 - Added `glfwGetGLXWindow` to query the `GLXWindow` of a window
 - Added icons to examples on Windows and OS X
 - Relaxed rules for native access header macros
 - Removed dependency on external OpenGL or OpenGL ES headers
 - Removed `_GLFW_USE_OPENGL`, `_GLFW_USE_GLESV1` and `_GLFW_USE_GLESV2`
   configuration macros
 - [Win32] Added support for Windows 8.1 per-monitor DPI
 - [Win32] Bugfix: Window creation would segfault if video mode setting required
                   the system to be restarted
 - [Win32] Bugfix: MinGW import library lacked the `lib` prefix
 - [Win32] Bugfix: Monitor connection and disconnection events were not reported
                   when no windows existed
 - [Cocoa] Removed support for OS X 10.6
 - [Cocoa] Bugfix: Full screen windows on secondary monitors were mispositioned
 - [X11] Bugfix: Monitor connection and disconnection events were not reported
 - [X11] Bugfix: Decoding of UTF-8 text from XIM could continue past the end
 - [X11] Bugfix: An XKB structure was leaked during `glfwInit`
 - [POSIX] Bugfix: An unrelated TLS key could be deleted by `glfwTerminate`
 - [WGL] Changed extension loading to only be performed once
 - [WGL] Removed dependency on external WGL headers
 - [GLX] Replaced legacy renderable with `GLXWindow`
 - [GLX] Removed dependency on external GLX headers
 - [GLX] Bugfix: NetBSD does not provide `libGL.so.1`
 - [EGL] Added `_GLFW_USE_EGLPLATFORM_H` configuration macro for controlling
         whether to use an existing `EGL/eglplatform.h` header
 - [EGL] Added and documented test for if the context is current on the calling
         thread during buffer swap
 - [EGL] Removed dependency on external EGL headers


## Contact

The official website for GLFW is [glfw.org](http://www.glfw.org/).  There you
can find the latest version of GLFW, as well as news, documentation and other
information about the project.

If you have questions related to the use of GLFW, we have a
[support forum](https://sourceforge.net/p/glfw/discussion/247562/), and the IRC
channel `#glfw` on [Freenode](http://freenode.net/).

If you have a bug to report, a patch to submit or a feature you'd like to
request, please file it in the
[issue tracker](https://github.com/glfw/glfw/issues) on GitHub.

Finally, if you're interested in helping out with the development of GLFW or
porting it to your favorite platform, join us on GitHub or IRC.


## Acknowledgements

GLFW exists because people around the world donated their time and lent their
skills.

 - Bobyshev Alexander
 - artblanc
 - arturo
 - Matt Arsenault
 - Keith Bauer
 - John Bartholomew
 - Niklas Behrens
 - Niklas Bergström
 - Doug Binks
 - blanco
 - Martin Capitanio
 - Chi-kwan Chan
 - Lambert Clara
 - Andrew Corrigan
 - Noel Cower
 - Jarrod Davis
 - Olivier Delannoy
 - Paul R. Deppe
 - Michael Dickens
 - Роман Донченко
 - Jonathan Dummer
 - Ralph Eastwood
 - Siavash Eliasi
 - Michael Fogleman
 - Gerald Franz
 - GeO4d
 - Marcus Geelnard
 - Eloi Marín Gratacós
 - Stefan Gustavson
 - Sylvain Hellegouarch
 - Matthew Henry
 - heromyth
 - Lucas Hinderberger
 - Paul Holden
 - Aaron Jacobs
 - Toni Jovanoski
 - Arseny Kapoulkine
 - Osman Keskin
 - Cameron King
 - Peter Knut
 - Eric Larson
 - Robin Leffmann
 - Glenn Lewis
 - Shane Liesegang
 - Eyal Lotem
 - Дмитри Малышев
 - Martins Mozeiko
 - Tristam MacDonald
 - Hans Mackowiak
 - Zbigniew Mandziejewicz
 - Kyle McDonald
 - David Medlock
 - Bryce Mehring
 - Jonathan Mercier
 - Marcel Metz
 - Jonathan Miller
 - Kenneth Miller
 - Bruce Mitchener
 - Jack Moffitt
 - Jeff Molofee
 - Jon Morton
 - Pierre Moulon
 - Julian Møller
 - Kamil Nowakowski
 - Ozzy
 - Andri Pálsson
 - Peoro
 - Braden Pellett
 - Arturo J. Pérez
 - Emmanuel Gil Peyrot
 - Cyril Pichard
 - Pieroman
 - Jorge Rodriguez
 - Ed Ropple
 - Aleksey Rybalkin
 - Riku Salminen
 - Brandon Schaefer
 - Sebastian Schuberth
 - Matt Sealey
 - SephiRok
 - Steve Sexton
 - Systemcluster
 - Dmitri Shuralyov
 - Daniel Skorupski
 - Bradley Smith
 - Julian Squires
 - Johannes Stein
 - Justin Stoecker
 - Elviss Strazdins
 - Nathan Sweet
 - TTK-Bandit
 - Sergey Tikhomirov
 - A. Tombs
 - Samuli Tuomola
 - urraka
 - Jari Vetoniemi
 - Ricardo Vieira
 - Simon Voordouw
 - Torsten Walluhn
 - Patrick Walton
 - Jay Weisskopf
 - Frank Wille
 - yuriks
 - Santi Zupancic
 - Jonas Ådahl
 - Lasse Öörni
 - All the unmentioned and anonymous contributors in the GLFW community, for bug
   reports, patches, feedback, testing and encouragement

