Directions for building the MSI

Download and install Wix 3.7RC: https://wix.codeplex.com/releases/view/98028
Add the Wix bin folder to your PATH environment variable (i.e. C:\Program Files (x86)\WiX Toolset v3.7\bin)
Unzip the attached zipfile and open a command prompt in the directory where you unzipped the files

Copy the latest RandoriCompilerPlugin.dll into the folder with the wxs.
Update the version number in the command below to match the RandoriCompilerPlugin.dll version.

Run these commands:
	
candle RandoriCompilerExtension.wxs -dPluginVersion=1.4.0 -ext WixNetFxExtension.dll
light RandoriCompilerExtension.wixobj  -ext WixNetFxExtension.dll
