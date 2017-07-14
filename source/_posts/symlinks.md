---
title: symlinks
date: 2017-07-14 18:13:21
tags:
---
---
title: Symlink sublime text
---
Welcome to [sublimetext.com](http://www.sublimetext.com/docs/2/osx_command_line.html)! voici le tutorial. 



Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).



#OS X Command Line

Overview

Sublime Text 2 includes a command line tool, subl, to work with files on the command line. This can be used to open files and projects in Sublime Text 2, as well working as an EDITOR for unix tools, such as git and subversion.

Setup

The first task is to make a symlink to subl. Assuming you've placed Sublime Text 2 in the Applications folder, and that you have a ~/bin directory in your path, you can run:

ln -s "/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl" ~/bin/subl
Usage

Run subl --help,
Usage: subl [arguments] [files]         edit the given files
   or: subl [arguments] [directories]   open the given directories
   or: subl [arguments] -               edit stdin

Arguments:
  --project <project>: Load the given project
  --command <command>: Run the given command
  -n or --new-window:  Open a new window
  -a or --add:         Add folders to the current window
  -w or --wait:        Wait for the files to be closed before returning
  -b or --background:  Don't activate the application
  -s or --stay:        Keep the application activated after closing the file
  -h or --help:        Show help (this message) and exit
  -v or --version:     Show version and exit

--wait is implied if reading from stdin. Use --stay to not switch back
to the terminal when a file is closed (only relevant if waiting for a file).

Filenames may be given a :line or :line:column suffix to open at a specific
location.
EDITOR

To use Sublime Text 2 as the editor for many commands that prompt for input, set your EDITOR environment variable:

export EDITOR='subl -w'
Specifying -w will cause the subl command to not exit until the file is closed.

MacPorts

If you have the MacPorts version of Python installed, then starting Sublime Text 2 via the subl will not work correctly. As a workaround, start Sublime Text 2 first via Finder, and then interact with it using subl.
********







## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/deployment.html)
