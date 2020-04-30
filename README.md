# Get-RemoteProgram
This script generates a list by querying the registry and returning the installed programs of a local or remote computer. It allows for retrieval of additional properties such as the uninstall string of an application as well.

## Original Author
Author: Jaap Brasser
Blog: http://www.jaapbrasser.com

## Current Version
Version: 1.5

## Created
2013-08-23

## Updated
2019-08-02

## Version History
* **Version 1.0** - Initial Upload
* **Version 1.1** - Feature Update: 
  * Correctly searches the Wow6432Node for 32 bit applications on 64 bit systems. 
  * Added a new parameter -Property to specify additional properties to be loaded from the registry. 
  * Added support for the pipeline to be used to supply the function with computernames
* **Version 1.2** - Fixed error messages when a base registry key was empty
* **Version 1.2.1** - Fixed errors on 32bit systems as reported by vsk2014
* **Version 1.3** - Added new parameters and added functionality to filter similar program names from the results
* **Version 1.4** - Feature Update: 
  * Updated object creation for PowerShell 3 and later
  * Added TCP test for connectivity to a system
  * Added four new parameters: LastAccessTime, IncludeProgram, ExcludeProgram
, ProgramRegExMatch, and Updated help documentation
* **Version 1.4.1** - Minor improvement: 
  * Added Array support for -IncludeProgram & -ExcludeProgram
* **Version 1.5** - Feature update:
  * Added -DisplayRegPath switch parameter, displays which registry key was queried for the program
  * Added -MicrosoftStore switch parameter, queries currentuser package list to also list installed Microsoft Store packages
  * Added Write-Verbose statement to follow what the script is querying
  * Now also queries HKCU, before only queried HKLM which did not provide a full list of installed programs

## Resources
* [Technet Script Center](https://gallery.technet.microsoft.com/scriptcenter/Get-RemoteProgram-Get-list-de9fd2b4)
