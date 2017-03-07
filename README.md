# oscpkt
Julien Pommier's Ultra minimalistic OSC library http://gruntthepeon.free.fr/oscpkt/

From the original project:
# Ultra minimalistic OSC library
## The Story
OscPkt is a very minimalistic [OSC](http://opensoundcontrol.org/introduction-osc) library. What I wanted to achieve with this lib:
* make it at small as possible. It consists of one header file, [oscpkt.hh](oscpkt.hh), which implements pretty much all of the OSC specification, 
even the pattern matching stuff (the wildcards etc).
* use only dumb, basic, c++. No boost stuff and no exceptions.
* make it robust with respect to malformed packets, and handle errors cleanly.
* make it portable on linux/macos/win32.
* release it under the zlib license, which basically allows you to do whatever you want except suing me.

Other OSC libraries: [liblo](http://liblo.sourceforge.net/) is the most well-known. This is a feature-complete osc library, 
written in C and LGPL licensed. 
Another well-known c++ OSC library is [oscpack](http://www.audiomulch.com/~rossb/code/oscpack/), BSD licensed, 
not feature complete (no pattern matching), with portable udp transport, but still a bit large for my taste (and it throws exceptions).

## The Code

Here is the code, approximately 650 lines of boring c++, in a single header file: [oscpkt/oscpkt.hh](oscpkt.hh) . 
It basically provides 3 classes: a class for reading/writing OSC messages, a packet reader for parsing 
incoming packets, and a packet writer for filling outgoing packets.

As a bonus, I also provide a header file for sending/receiving these packets over UDP: 
[oscpkt/udp.hh](upd.hh). Very basic, but works on linux/macos/win32.

And finally a test file [oscpkt/oscpkt_test.cc](oscpkt_test.cc) with a bit of fuzzing, and a very basic demo file
[oscpkt/oscpkt_demo.cc](oscpkt_demo.cc).

All these four files are gathered into a single, shiny, tar.gz archive (the only changes with respect to version 1.0 a 
a few compil fixes for mingw and warning fixes).

## The Code

Yay there is even a doxygen generated doc, mostly useless and a bit redundant with this page:
[doxygen doc here](http://gruntthepeon.free.fr/oscpkt/html).


