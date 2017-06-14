# godot.msi

Test build scripts for godot tools msi packages

To compile MSI you will need:
1. [Wix Toolset](http://wixtoolset.org) to be installed
2. Add toolset bin folder to system PATH variable (mine was under *C:\Program Files (x86)\WiX Toolset v3.11\bin*)
3. Clone this repository.
4. Drop in prebuilt **godot.windows.tools.64.exe**
5. Drop in prepared **godot.ico** (have used [ImageMagic](http://www.imagemagick.org) to convert png to ico with command **magick convert icon.png -define icon:auto-resize=64,48,32,16 godot.ico**)
6. Open command prompt and run **candle godot.wxs -dexe_path=godot.windows.tools.64.exe -dversion=3.0.0.0** 
7. And then **light godot.wixobj**

Note that we set variable **exe_path** to be used by [preprocessor](http://wixtoolset.org/documentation/manual/v3/overview/preprocessor.html) by prefixing it with **-d**.

## Important
 * Only [Major.Minor.Build](https://msdn.microsoft.com/en-us/library/windows/desktop/aa370859(v=vs.85).aspx) version number parts matter in MSI versioning (and is limited to [0-255].[0-255].[0-65535]).
 * All [GUID's](https://msdn.microsoft.com/library/aa368767.aspx) used should be upper case.