# SmallBASIC syntax coloring for Sublime Text

This Sublime Text package adds syntax coloring and indentation rules for the SmallBASIC language (https://smallbasic.github.io/)

![Example](https://github.com/Joe7M/smallbasic.sublimetext.syntaxcoloring/blob/main/screenshot.png)

## Features:

- Syntax coloring
- Indentation rules
- Script execution

## Installation

Copy the files in the folder "package" to the User directory in the Sublime Text package folder. The Sublime Text package folder can be open with Sublime Text under Preferences -> Browse Packages.

## Script execution

Please edit the file `SmallBASIC.sublime-build` to configure scipt execution.

### Linux 

The default file launches sbasicg (SDL-version) in Linux. sbasicg must be in the search path.

```
{
	"cmd": ["cmd", "/c", "sbasicg", "-r", "$file"],
	"selector": "source.SmallBASIC"
}
```

Replace sbasicg by sbasic if you want to launch the console version. You can also include the full path.

```
{
	"cmd": ["cmd", "/c", "sbasic", "$file"],
	"selector": "source.SmallBASIC"
}
```

### Windows

Replace sbasicg by sbasicg.exe. You can include the full path if sbasicg.exe is not in the search path.

```
{
	"cmd": ["cmd", "/c", "sbasicg.exe", "-r" "$file"],
	"selector": "source.SmallBASIC"
}
```
