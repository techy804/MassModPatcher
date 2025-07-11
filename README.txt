README

Section 1: Operation Instructions
	
	Part 1.1: Common
		1.1.1 First Enter in the path of the vanilla data.win of the file. If you just want to dump and combine already prepared modded data.win files, enter "skip" into this field. Hit Enter. 
		1.1.2 Then enter in the amount of mods you want to operate on as an integer (e.g. "2" for 2 mods).
	Part 1.2: Mass Apply Patches
		1.2.1 One at a time, enter in the path of your xDelta patches, hitting enter in between each one.
		1.2.2 Wait for xDelta3 to finish patching the data.win files
		1.2.3 If you just wanted to make a ton of single-mod data.win copies of your game, you may exit the terminal now
	Part 1.3: Dump and Combine
		1.3.1 Hit Enter, unless you want to dump and import manually or you have your own version of UTMT CLI that you prefer. If you want to use your own version of UTMT CLI, enter in the path for that. If you want to dump and import manually, enter "skip".
		1.3.2 Once it is done dumping, hit enter
		1.3.3 wait for the app to compare the modded files to the vanilla files, hit enter once it is finished, it will then import the difference
		1.3.4 It will ask you if you would like to link imported code, hit "y"
		1.3.5 It will ask you what you would like to name your pack, enter anything you please.
		1.3.6 Your completed pack is located at \output\result\*pack name*\
		1.3.7 Once you hit enter again, the program will delete output\xDeltaCombiner and close. You may close via Alt+F4 or hitting the "X" on the window if you don't want to delete them, but you will need to manually delete the folder on next use. 

Section 2: Technical Information
	Part 2.1: System Requirements
		2.1.2: System Requirements
			OS: Windows 8.1
			CPU: x86_64
			Storage: 256MB
			RAM: 192MB
			Software: .NET 8.0 runtime
		2.1.3: System Recommended
			OS: Windows 11
			Storage: 2GB
			RAM: 512MB	
	Part 2.2: output directory structure
		xDeltaCombiner\0: Vanilla Folder
		xDeltaCombiner\1: Finished Product Folder
		xDeltaCombiner\(2+): Single Mod Folder
		xDeltaCombiner\#\Objects: GameMaker Objects location
		result\: resulting merges
		modNumbersCache.txt: used to pass off a variable value from GM3P to UTMTCLI during runtime. 
	Part 2.3: Known Issues and limitations
		Issue: Sprites that are not in the vanilla game may be out of order, except for the last mod applied.
		Issue: Backported mods don't compare correctly
		Limitation: Can only apply patches meant for the same version of the same game. Can't mix and match
		Limitation: If 2 mods modify the same object, only the changes for the last affect mod entered applies.
		Haven't implemented yet: Error Handling
		Haven't implemented yet: a way for the user to turn off verbosity
		Found a bug not written here? Use GameBanana Issues or GitHub Issues to report it.
	Part 2.4: Tools used
		xDelta3 CLI for applying mods
		A custom version of UndertaleModTool for dumping and importing GameMaker Objects
		VS2022 to make and build this program
		This program was poorly written in C# .NET
		SHA1 Hashing was used for comparing files

Section 3: Installation and run Instructions
	Part 1: Common for both methods
		3.1.1 Make sure you have the .NET runtime v8.0 or later installed
		3.1.2 Once downloaded the .zip folder, extract it to it's own folder
	Part 2: Run via command line/terminal
		3.2.1 use the "ls" and "cd" commands to navigate to the extracted folder
		3.2.2 type ".\GM3P.exe" to run the program
	Part 3: Run via File Explorer
		3.3.1 navigate to the extracted folder
		3.3.2 double-click "GM3P.exe"