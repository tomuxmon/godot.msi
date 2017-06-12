# godot.msi

Test build scripts for godot tools msi packages

To compile MSI you will need:
1. [Wix Toolset](http://wixtoolset.org) to be installed
2. Add toolset bit folder to system PATH variable (mine was under *C:\Program Files (x86)\WiX Toolset v3.11\bin*)
3. Clone this repository.
4. Drop in prebuilt **godot.windows.tools.64.exe**
5. Drop in prepared **godot.ico** (have used [ImageMagic](http://www.imagemagick.org) to convert png to ico with command **magick convert icon.png -define icon:auto-resize=64,48,32,16 godot.ico**)
6. open command prompt and run **candle godot.wxs** and then **light godot.wixobj**