# About Rosette for Excel (Beta)
Rosette for Excel is a plugin that makes the features of the [Rosette API](https://developer.rosette.com/) available to Excel users code-free. The Rosette API provides text analytics, natural language, and names processing tools for a variety of use cases and is developed by [Basis Technology Corp.](http://www.basistech.com/)
# Known System Requirements
- .NET 4.0 or greater.  To check your available versions:
    - Open a command window
    - Type in ```dir %windir%\Microsoft.NET\Framework /AD```
    - If necessary, install from [Microsoft .NET Framework 4.5.2](https://www.microsoft.com/en-us/download/details.aspx?id=42642)
# How to Install
Currently, Rosette for Excel is only compatible with Windows OS. The beta release has been tested in Office 2010, 2013, 2016 on Windows 7 & 10, with broader support on its way for the upcoming official GA release.
To install:
- Click the [releases](https://github.com/rosette-api-community/rosette-for-excel/releases) tab in the Rosette for Excel repository
- Click the link to the latest release
- Under "Downloads" click RosetteForExcel.msi
- Once the .msi file has downloaded, double click to install. The installation is "per user", so no elevated permissions should be required.

# Getting Started
Before you can actually start using the plugin, you’ll need an active Rosette API key. If you don’t already have a Rosette API developer account, head to [developer.rosette.com](http://developer.rosette.com/signup) to get your free Rosette API key. Complete the sign-up and activation process. Back in Excel, navigate to the Rosette ribbon tab and enter your key in the "API Key" dialog. Check your connection by clicking "Check Key." If a green check appears, you’re good to go! An alternate URL can be specified for Rosette On-Premise users, but is not required. For more information on using the plugin and its various features, check out the Use Info guide [here](UseInfo.md) and the Quick Start Guide [here](QuickStartGuide-NameTranslation.md).
