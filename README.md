JCAimbot - Java Colour Aimbot
========

To do
--------
* Implement mouse movement and test it moves as expected - need mouse 'fuzzing'
* Get default pixel values from skins
* Implement scanning bufferedimage and getting pixel values
* Implement mouse click with toggle button (autoshoot)
* Aim-assist activated by keypressed (i.e. hold button)
* Implement button to redefine searched pixel values with pixel at centre to allow adjustment
* Only capture small area around centre for better efficiency?
* Pixel values may change due to lighting etc. - work out what brightness should be, put in tolerances?



Known Issues
--------------
* Mouse position is locked once moved, so it won't move - therefore move to a pixel ±a few pixels near the actual desired location to allow for an approximate aim assist (i.e. 'fuzz' the movement). Will implement soon.

* ~~Fails to detect keypress despite boolean flag being set, unless boolean flag is first printed to terminal, then it works because magic.~~ - Fixed by use of volatile keyword as it prevents local the variable being thread-locally cached, see: http://www.javamex.com/tutorials/synchronization_volatile.shtml (03/02/2013)

Notes
-------
* Mouse position is always held at the centre by the game (i.e. for 1024x768 res it's held at 512, 384)
