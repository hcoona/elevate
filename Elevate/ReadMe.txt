This is a fork project from http://code.kliu.org/misc/elevate/

elevate - Command-Line UAC Elevation Utility
==================================

This utility executes a command with UAC privilege elevation. This is useful for working inside command prompts or with batch files.

Usage
====================

elevate [(-c | -k) [-n] [-u]] [-w] command

Options:
  -c  Launches a terminating command processor; equivalent to "cmd /c command".
  -k  Launches a persistent command processor; equivalent to "cmd /k command".
  -n  When using -c or -k, do not pushd the current directory before execution.
  -u  When using -c or -k, use Unicode; equivalent to "cmd /u".
  -w  Waits for termination; equivalent to "start /wait command".

For more information, please consult the readme.txt file found inside the package.

Features
====================

Although there are a number of other tools that serve the same purpose, this particular utility has several features that set it apart from the rest:

    Correct handling of command line parameters; the command line parameters are passed along for execution verbatim, without being chopped up and reassembled.
    The ability to launch the command processor using /c instead of /k.
    The ability to launch the command processor in the current directory.
    Better error messages to make troubleshooting execution problems easier.
    Native C code avoids the burdensome .NET startup overhead and allows for a much smaller executable file size.

Windows Vista (or newer) is required.