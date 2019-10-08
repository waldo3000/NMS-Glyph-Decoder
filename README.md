# Glypher
## Decodes No Man's Sky location from on-screen symbols

Glypher is a Windows command line program that decodes and exports the No Man's Sky portal glyphs seen on the bottom of the screen in photo mode.  These glyphs can be used to create a log of visited places or they can be used to map the locations of black holes.

With this program, you do not need to retype coordinate information or use Signal Boosters to get the coordinates.  It even works in space before you have landed your ship.

### Setup
Unzip the glypher.zip archive to any convenient place.  I'll call the path name to this program "glypher_path".
The program must be told where to find the NMS screenshot files.  To view/change this on Steam, use the Steam application on PC and go to Settings/In-Game/Screenshot Folder and it will tell you the path.  I'll call this "screenshot_path".
	
Using a text editor, make a file consisting of a single line like this:

	glypher_path\glypher.exe screenshot_path
	
Your actual file could be something like this (but your file will differ):

	c:\users\waldo\desktop\glypher\glypher.exe "C:\Program Files (x86)\Steam\userdata\xxxxxxxxx\760\remote\275850\screenshots"

Name this batch file with a .bat extension and place it in a convenient place.  Remember to use quotes around any path name that has spaces in it.

### Usage
To run the program, double-click the batch file icon.  A console window will open and the current galactic coordinates will be shown (if present in the most recent screenshot).  Glypher will also export the galactic address to the clipboard.  Move to your favorite spreadsheet, click in the desired cell, and paste.

A more interesting use case is to use Glypher while playing NMS.  If you leave the Glypher window open, the program will run in the background, monitoring the screenshot folder for changes.  If Glypher sees a change in the screenshot folder, it will attempt to decode the glyphs in the most recent screenshot.  It will make a short beep if it successfully decodes the glyphs in the image and it will be silent if anything went wrong.  

To create a screenshot that contains the glyphs, open Photo Mode in NMS to enable the glyphs on the screen, then press the Steam "Screenshot Shortcut Key" (F12 by default) to make the screenshot.  After the screenshot is written to disk, the clipboard contents will reflect the coordinates in the on-screen glyphs.

You can add "-portal" to the end of the command line to show/copy the coordinates in portal coordinate format instead of galactic address format.

### Tips
After pasting a portal code to a program such as Excel, you can reformat that cell using the NMS Glyph font from https://www.reddit.com/r/NoMansSkyTheGame/comments/97w347/download_nmsglyphs_fonts_for_your_banners/ to see the glyphs as symbols rather than as hex codes.

Darker backgrounds in the lower left portion of the screen work best.  PNG format screenshots are preferred due to not using lossy compression (check "Save an uncompressed copy" in the Steam settings).

You could put a shortcut to your batch file in the Windows Startup folder if you want Glypher to run each time at startup.

