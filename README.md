# Unlocker 1.9.0.1
Able to run UnlockerPortable without SplashScreen

-------------------------------
BACKGROUND STORY
-------------------------------
The original "Unlocker" program comes from Cedrick Collomb.
However, a modified version from "PortableAppZ" is the only version,
that works without problems on today's computers.

Unfortunately, the portable one contains a SplashScreen (advertising banner) for it, which is displayed at every start. Changing the INI file to <DisableSplashScreen=true> only works as long as the file path is not changed, in the subfolder of the additional INI this is also and <LastDirectory=C:\InnoSetup-Software\Unlocker> is also correct there.
is also correct there. If existing INI files are changed after changing the path and not recreated, PortableAppZ will notice this as well. In all cases the SplashScreen will still be displayed and for the future it will also be enabled again in the INI file for the future. This was not particularly forward-looking by "PortableAppZ" programmed, especially since it is quite offensive with regard to the copyright of the actual developer Cedrick CCollomb. it is quite offensive. However, maybe it was just a bug, because other portables don't seem to be so stubborn....

-------------------------------
HOW IT WORKS TECHNICALLY:
-------------------------------
My modification don't change the original code (neither from Cedrick Collomb nor from PortableAppZ). It protects the copyright in the sense of it's origin developer and allow silent operation without any ads for everybody. Therefore before the start of "UnlockerPortable.exe" a VBS-Script re-creates the correct two files named "UnlockerPortable.ini" (one in root and one in subfolder "Data") with the command not to show SplashScreen and information about the LastDirectory (the actual path has to be there for really not to show the SplashScreen).

In other words: It realizes a fix to what PortableAppZ meant the software has always to be, providing the INI file, but for a unknown reason malfunctioned up to now.


-------------------------------
USAGE:
-------------------------------
-Both method 1 and 2 are portable solutions-

Method 1 (release): Download the release EXE which doesn't accept the command line options but as single file is full portable and perfectly suitable for USB flash drives. Recommended for everyone who likes to use the graphical interface (GUI). Command-line parameters (console) from Unlocker won't work here.

Method 2 (developer): Download the "bin" folder from Repositories if you want to achieve automatic operations using the command line. In this case you have to run the VBS "DisableSplash.vbs" first before "UnlockerPortable.exe" with parameters (run >> "UnlockerPortable.exe" -h << to list all arguments).
