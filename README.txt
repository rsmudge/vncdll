=======================================================
= Stand-alone VNC server compiled as a Reflective DLL =
=======================================================

This VNC server distribution is a derivative of the VNC server distributed with 
the Metasploit Framework:

https://github.com/rapid7/metasploit-framework/tree/master/external/source/vncdll

The changes are as follows:

1) This VNC server distribution does not implement session tracking or the 
   other nifty features courtesy of the vncdll wrapper provided with the 
   Metasploit Framework. This simplifies the code a great deal (and its one less 
   thing that can go wrong)

2) The MSF VNC Server is designed for delivery with a bind or reverse TCP 
   stager. This VNC server assumes its injected as-is and opts to bind to
   localhost and a hard-coded port. See line ~133 of winvnc/vncdll.cpp

License: GPLv2

See LICENSE.txt for more information
