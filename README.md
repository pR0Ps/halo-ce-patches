Halo CE Patches
===============

A `.crk` file that defines byte-level patches for Halo CE v1.0.10

Patches
-------
- Make LAA (large address aware), allowing it to use up to 4GB of RAM (normal limit is 2GB).
- Remove DRM and key checks: Allows playing and hosting games without a valid CD key. Pretty much a
  requirement now since the game was released in 2004 and is no longer available for purchase.
- Bind server to 0.0.0.0 instead of the (poorly) auto-detected local IP: Fixes hosting servers on
  computers with multiple network interfaces.
- Disable setting an "exit flag" in the registry.
- Continue to draw the screen when focus is lost: Useful when playing in windowed mode.
- Disable gamma modification: Prevents the game from setting the OS-level brightness.
- Disable auto-centering the crosshair in vehicles: This disables the game automatically pulling
  your crosshair to the center of the screen.
- Disable mouse acceleration.
- Block checking for game updates.

With all the patches applied, no registry modifications will be made by the game. This is ideal for
a portable executable.

Applying the patches
--------------------
- I wrote [`pycrk`](https://github.com/pR0Ps/pycrk) while working on this to make applying/removing
  patches simple. It's a CLI application written in Python that can list, apply, and remove patches
  described by a `.crk` file.
- [CRACKER v.002b](https://forum.exetools.com/showthread.php?t=18773) is a Win32 GUI application
  that supports `.crk` patches. No source code provided.  I ran it in a sandboxed environment on the
  off-chance it was malicious. You probably should too.
- It's also possible to open the `.crk` file in a text editor and use a hex editor to manually edit
  the bytes in the executable. It just sucks.

Credits
=======
The [Chimera project](https://github.com/Kavawuvi/chimera) provides a lot of documentation,
signatures, and other data on Halo CE. It was super helpful in developing these patches.

License
=======
All content is licensed under the [GNU GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html)
