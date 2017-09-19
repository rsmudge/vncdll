=======================================================
= Stand-alone VNC server compiled as a Reflective DLL =
=======================================================

This VNC server distribution is a derivative of the TightVNC server distributed with 
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

3) This VNC server happily lives in its current desktop context and does not
   try to switch to another context. This allows the server to function, as 
   expected, when injected into a process associated with another desktop
   session.

Build Instructions: Open a Visual Studio cmd.exe session. Type 'make'.

License: GPLv2

See LICENSE.txt for more information

These changes:

	Copyright (C) 2017 Strategic Cyber LLC

Rapid7's Changes (Metasploit Framework):

	Copyright (C) 2006-2010, Rapid7, Inc

TightVNC 1.3.10 (see winvnc\README.txt):

	Copyright (C) 1999 AT&T Laboratories Cambridge.
	Copyright (C) 2000 Tridia Corp.
	Copyright (C) 2002-2003 RealVNC Ltd.
	Copyright (C) 2001-2004 HorizonLive.com, Inc.
	Copyright (C) 2000-2006 Constantin Kaplinsky.
	Copyright (C) 2000-2009 TightVNC Group
	All rights reserved.
