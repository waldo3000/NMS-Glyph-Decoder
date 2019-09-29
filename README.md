# NMS-Glyph-Decoder
Decodes No Man's Sky location from on-screen symbols

Glypher is a Windows command line program that decodes and exports the No Man's Sky portal glyphs seen on the bottom of the screen in photo mode.  These glyphs are used with the portals to transport to another location.  In addition, they can be converted to galactic coordinates for use with other third-party utilities.  I made Glypher to help record places I have visited.  It can also be useful when doing Black Hole Suns mapping.

With this program, you do not need to retype coordinate information or use Signal Boosters to get the coordinates.  It even works in space before you have landed your ship.

How to Use:
	Unzip the glypher.zip archive to any convenient place.  I'll call the path name to this program "<glypher path>"
	The program must be told where to find the NMS screenshot files.  To view/change this on Steam, use the Steam application on PC and go to Settings/In-Game/Screenshot Folder and it will tell you the path.
	I'll call this "<screenshot path>".
	Using a text editor, make a file consisting of a single line like this:
		<glypher path>\glypher.exe <screenshot path>
	Name this batch file with a .bat extension and place it in a convenient place.
	You should now have a file that has one line that says something like:
		c:\users\waldo\desktop\glypher.exe "C:\Program Files (x86)\Steam\userdata\xxxxxxxxx\760\remote\275850\screenshots"
	Your file will differ.  Remember to use quotes around any path name that has spaces in it.
	
	To run the program, double-click the batch file icon.  A console window will open and the current galactic coordinates will be shown (if present in the most recent screenshot).  Glypher will also export the address to the clipboard.  Move to your favorite spreadsheet, click in the desired cell, and paste.
	
	While in the game, open Photo Mode to see the glyphs on the screen, then press the Steam "Screenshot Shortcut Key" (F12 by default) to make a screenshot that contains the glyphs.  If you leave the Glypher window open, the program will run in the background, monitoring the screenshot folder for changes.  If it sees a change, it will attempt to decode the glyphs each time another screenshot is made.  It will make a short beep if it successfully decodes the image and it will be silent if anything went wrong.
	
	You can add "-portal" to the command line to show/copy the coordinates in portal coordinate format. After pasting the portal code to a program such as Excel, you can reformat that cell using the NMS Glyph font from https://www.reddit.com/r/NoMansSkyTheGame/comments/97w347/download_nmsglyphs_fonts_for_your_banners/ to see the glyphs as symbols rather than as hex codes.

	Darker backgrounds in the lower left portion of the screen work best.  Both JPEG and PNG files work, but PNG works better due to not being compressed (check "Save an uncompressed copy" in the Steam settings).
	
	This version of Glypher only knows about 1920 x 1080 (FHD) images, but I can add other resolutions if there is a demand for that.
	
You can download the program from GitHub at:
	TBD (executable)
