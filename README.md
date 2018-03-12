## Process Hacker

A free, powerful, multi-purpose tool that helps you monitor system resources, debug software and detect malware.

[![Build status](https://ci.appveyor.com/api/projects/status/5einmgmy3mnsfjdn?svg=true)](https://ci.appveyor.com/project/processhacker/processhacker2)
[![Licence](https://img.shields.io/badge/license-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.en.html)

![Logo](https://raw.githubusercontent.com/processhacker2/processhacker/master/ProcessHacker/resources/ProcessHacker.png)

* [Official Website](http://processhacker.sourceforge.net/)
* [FAQ](http://processhacker.sourceforge.net/faq.php)
* [Nightly Builds](https://wj32.org/processhacker/nightly.php)

## System requirements

Windows 7 or higher, 32-bit or 64-bit.

## Features


* A detailed overview of system activity with highlighting.
* Graphs and statistics allow you quickly to track down resource hogs and runaway processes.
* Can't edit or delete a file? Discover which processes are using that file.
* See what programs have active network connections, and close them if necessary.
* Get real-time information on disk access.
* View detailed stack traces with kernel-mode, WOW64 and .NET support.
* Go beyond services.msc: create, edit and control services.
* Small, portable and no installation required.
* 100% [Free Software](http://www.gnu.org/philosophy/free-sw.en.html) ([GPL v3](http://www.gnu.org/licenses/gpl-3.0.en.html))


## Additional information


You cannot run the 32-bit version of Process Hacker on a
64-bit system and expect it to work correctly, unlike other programs.



## Enhancements/Bugs


Please use the official [GitHub issue tracker](https://github.com/processhacker2/processhacker/issues)
for reporting problems or suggesting new features.

For my extended build use the my [GitHub issue tracker](https://github.com/VictorVG/PH/issues)


## Settings

If you are running Process Hacker from a USB drive, you may want to
save Process Hacker's settings there as well. To do this, create a
blank file named "ProcessHacker.exe.settings.xml" in the same
directory as ProcessHacker.exe. You can do this using Windows Explorer:

1. Make sure "Hide extensions for known file types" is unticked in
   Tools > Folder options > View.
2. Right-click in the folder and choose New > Text Document.
3. Rename the file to ProcessHacker.exe.settings.xml (delete the ".txt"
   extension).

## Plugins

Plugins detected on Process Hacker startup and can be configured from
Hacker > Plugins and Options using Process Hacker settings editor.

If you experience any crashes involving plugins, make sure they
are up to date.

Disk and Network information provided by the ExtendedTools plugin is
only available when running Process Hacker with administrative
rights.

## KProcessHacker

Process Hacker uses a kernel-mode driver, KProcessHacker, to
assist with certain functionality. This includes:

* Capturing kernel-mode stack traces
* More efficiently enumerating process handles
* Retrieving names for file handles
* Retrieving names for EtwRegistration objects
* Setting handle attributes

Note that by default, KProcessHacker only allows connections from
processes with administrative privileges (SeDebugPrivilege). To allow Process Hacker
to show details for all processes when it is not running as administrator:

1. In Registry Editor, navigate to:
   HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\KProcessHacker3
2. Under this key, create a key named Parameters if it does not exist.
3. Create a DWORD value named SecurityLevel and set it to 0 then is not signed build.
4. Restart the KProcessHacker3 service (sc stop KProcessHacker3, sc start KProcessHacker3).
