# Spec for ttfautohint control file GUI

Proposed workflow:

1. Open a font in a Windows testing environment
2. Find a glyph where you need to make tweaks
3. Open that font in Glyphs
4. Open that glyph
5. Run the script which will have a GUI for tweaks
6. Hit save in the script window which will create a control file for ttfautohint
7. Use that file in ttfautohint

## What I think needs to happen in the script/plugin

1. `#` comment glyph name
1. Get glyph ID from open glyph
2. User selects point size to alter
2. User selects glyph node to alter
3. GUI displays some options, such as:  
	a. snap node to height (baseline, x-height, etc)
	b. decrease or increase stem thickness
	c. move height +/- `x` pixels
4. User hits save, writing file
5. Repeat process with different glyph, appending info to control file

(All information is written to temp file after each step and adjustment in GUI)
