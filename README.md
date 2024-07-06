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

By default, the script reads files from the `svg` folder. Several example files have been included therein.




## Limitations

- Fonts are monochrome only. Building color fonts requires a more advanced tool like [nanoemoji](https://github.com/googlefonts/nanoemoji)
- Source svgs need to all have the same size viewbox for best results. (Fontforge can be set up to autoscale imported outlines, but that was giving me strange results, and so this script does not take advantage of that functionality.)
- One of the svg files must be specified as the placeholder geometry, which is to be used when ligatures contain a codepoint without an associated file.
- Sometimes the outlines combine in unintended ways when overlapping. It may be helpful to combine objects in the svg before building the font.



## License

The script itself is released under a [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) license. 
If you redistribute the script or a derivative, please provide attribution.

I claim no ownership over any fonts you create with this, nor do I require attribution if you don't redistribute the script itself.
That said, if you use this, I would like to see what you make! You can [leave a comment here](https://github.com/RobertWinslow/Simple-SVG-to-Font-with-Fontforge/issues/2) showing off your work.


