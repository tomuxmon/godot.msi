# godot.msi

Test build scripts for godot tools msi packages

To compile MSI you will need:
1. [Wix Toolset](http://wixtoolset.org) to be installed
2. Add toolset bit folder to system PATH variable (mine was under *C:\Program Files (x86)\WiX Toolset v3.11\bin*)
3. open cmd and run *candle godot.windows.tools.64.wxs* and then *light godot.windows.tools.64.wixobj*