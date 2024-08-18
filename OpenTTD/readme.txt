OpenMSX Readme - An OpenTTD Music replacement set

===============================
Current Version: OpenMSX 0.3.1
===============================

Contents
0 About OpenMSX
1 Installing
2 Troubleshooting
3 Contributing and compiling from source
4 License
5 Credits



0 About OpenMSX
===============

OpenMSX is an open source replacement for the original Transport Tycoon Deluxe
(TTD) music. All contributions are licensed under the GPL v2.



1 Installing
============

1. First, make sure that you downloaded and installed at least OpenTTD version
1.0.0 or later.

2. 
a) Manually:
Next, download the latest OpenMSX package. There are a few sources:
- the development homepage http://bundles.openttdcoop.org/openmsx
- Look for "OpenMSX" on one of the OpenTTD binaries servers, it is found in the
"bananas" section:
http://binaries.openttd.org/bananas/OpenMSX-0.2.1.tar.gz (or possibly with a
newer version).

Unpack the zip file into the OpenTTD /gm directory (see section 4.2 of the
OpenTTD readme for a detailed treatise on all data dirs OpenTTD recognizes).
- An OpenTTD folder in your user account's home directory:
	Windows:	C:\My Documents (95, 98, ME)
			C:\Documents and Settings\<username>\My Documents\OpenTTD (2000, XP)
			C:\Users\<username>\Documents\OpenTTD (Vista, 7)
	Mac OSX: ~/Documents/OpenTTD
	Linux:   ~/.openttd
- The OpenTTD installation directory.

b) Via ingame content download:
- Go to the content download, and search for OpenMSX; it's found in the baseset
category.

3. In the main menu of the game, click the Game Options  button. The Game
Options  dialog will appear.

4. Select OpenMSX  from the drop-down list below Base Music set if that's not
selected already (bottom left of window). Close the window using the × in the
upper left corner.

Now that wasn't so hard, was it? Anyways, if you're having trouble getting
OpenMSX to work, please file a detailed report on what you did, what error
messages you got and where you got stuck at our bug tracker at
http://dev.openttdcoop.org/projects/openmsx or in the tt-forums.



2 Troubleshooting and bad sound output
======================================

Depending upon the hardware and the music driver used, OpenTTD may have problems
to playback some songs without error or that it may happen that subsequent sound
output is changed in a detrimental way. The latter is especially know to happen
with the windows "dmusic" sound driver. You may want to try the "win32" music 
driver, if you have problems with windows' default dmusic driver. Search your
openttd.cfg for "musicdriver" and change the line to "musidriver = win32".
Consult also the OpenTTD readme for available options and its known-bugs.txt
for a more detailed and possibly more up to date description of windows music
driver issues.



3 Contributing and compiling from source
========================================

The OpenMSX source is available in a Mercurial repository or as gzip'ed tarball.
You can do an anonymous checkout from http://mz.openttdcoop.org/hg/openmsx ,
e.g. using
   hg clone http://mz.openttdcoop.org/hg/openmsx or obtain the tarball from
http://bundles.openttdcoop.org/openmsx/releases.
   
Prerequisites to building OpenMSX:
- mercurial (only when not building from a tarball, available from
http://mercurial.selenic.com/wiki/Download?action=show&redirect=BinaryPackages)
- md5sum (linux, mingw) or md5 (mac)
- some gnu utils: make, cat, sed
- unix2dos for convenient conversion of the text files
- python (if you use mercurial, you'll have python)
and you might additionally want a text editor of your choice and possibly a
programme capable of creating and editing midi files.

On Windows: we advise to get a mingw development environment, download mercurial
from the sources mentioned above) For more detailed instructions see our guide
at http://dev.openttdcoop.org/projects/home/wiki and the very extensive and
detailed installation instructions on the mingw wiki at
http://www.mingw.org/wiki/Getting_Started

On Linux: your system should already have most tools, you'll probably only
mercurial available from the source mentioned above. For installation
instructions concerning mercurial refer to the manual of your distribution.

On Mac: Install the developers tools. Mercurial is easiest insalled via
macports: sudo port install mercurial

The use of mercurial is strongly encouraged as only that allows to keep track of
changes.

Once all tools are installed, get a checkout of the repository and you can build
OpenMSX using make. The following targets are available:
- all: builds all grfs and the obm file
- install: build and then copy OpenMSX in your OpenTTD music directory. Use
Makefile.local to specify a different path
- clean: cleans all generated files
- mrproper: also cleans generated directories
- bundle_src: create a source tarball
- bundle_zip: create a zip archive of OpenMSX
- bundle_bz2: create a bzip2 archive of OpenMSX
- bundle_tar: create a tar archive of OpenMSX
- check: checks the md5 sums of the built grf and obg files against those of
the official release versions

Given the usual case that you modify something within OpenMSX and want to test
that, a simple 'make install' should suffice and you can immediately test the
changes ingame, if you selected the nightly version of OpenMSX. Given default
paths, a 'make install' will overwrite a previous nightly version of OpenMSX.
Mind to re-start OpenTTD as it needs to re-read the grf files.



4 License
=========

OpenMSX Music Replacement Set for OpenTTD Copyright (C) 2010 OpenMSX Authors
(see below or in the source in themes.list) and is licensed under GPL v2.

This program is free software; you can redistribute it and/or modify it under
the terms of the GNU General Public License version 2 as published by the Free
Software Foundation.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program; if not, write to the Free Software Foundation, Inc., 1 Franklin
Street, Fifth Floor, Boston, MA 02110-1301 USA.



5 Credits
=========

OpenMSX is created by the following people (in order of the song list):

programming and coordination   Ingo von Borstel (planetmaker)
music critic and advisor:      kamnet
tttheme2.mid:                  -lucas-
big_man_boogie_redfarn.mid:    Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm)
ttsong_iv_imuh3.mid:           imuh3
modern_motion.mid:             Kyle Timmerman (Mr.Ksoft)
busy_schedule.mid:             mimm
the_fast_route.mid:            mimm
ttsong_iii_imuh3.mid:          imuh3
train_filled_with_cash.mid:    imuh3
flying_scotsman.mid:           imuh3
chuggachugga.mid:              imuh3
the_hobo_redfarn.mid:          Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm)
ultimate_run.mid:              Tistou Blomberg
midnight_snow_run.mid:         Tistou Blomberg
run_for_your_life.mid:         Tistou Blomberg
coconut_run2.mid:              Tistou Blomberg
harp_harmony.mid:              Tistou Blomberg
mighty_giant_run.mid:          Tistou Blomberg
wood_whistles.mid:             Tistou Blomberg
linns_basket.mid:              Tistou Blomberg
relax_song.mid:                Tistou Blomberg
chemistry_lab.mid:             Tistou Blomberg
5432gone_redfarn.mid:          Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm)
boogi_marabi_redfarn.mid:      Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm)
moo_redfarn.mid:               Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm) inspired by Cow Cow Boogie by Benny Carter, Gene de Paul, and Don Raye
say_what_redfarn.mid:          Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm)
be_sharp_bw_redfarn.mid:       Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm)
careless_perc_redfarn.mid:     Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm) traditional song
mosey_along_redfarn.mid:       Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm)
slow_neasy_redfarn.mid:        Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm)
city_blues_redfarn.mid:        Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm)
no_work_song_redfarn.mid:      Jim Redfarn (http://homepage.ntlworld.com/jim.redfarn/MidiPage.htm)
