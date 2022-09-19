# Simple-SVG-to-Font-with-Fontforge

This script uses FontForge to build a very basic monochrome font from a folder of SVG files.
Each SVG file must be named with the codepoint of the unicode character it is to be mapped to. 
    EG `1F94B.svg`
If a glyph maps to a sequence of codepoints, seperate the codepoints with `-` in the SVG file's name.
    EG `1F468-200D-1F9B3.svg`
If there are codepoints which are part of a sequence but lack their own SVG, then placeholder geometry is used.

See here for documentation about FontForge's scripting library:
https://fontforge.org/docs/scripting/python/fontforge.html


## Requirements

[FontForge](https://fontforge.org/en-US/), and its included python installation.


## Use

1. Adjust the global parameters in the first section of `build_simple_black_font_with_fontforge.py`
2. type `fontforge -script build_simple_black_font_with_fontforge.py` in the terminal.

