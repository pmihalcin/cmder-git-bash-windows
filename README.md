I use Windows machine in my job and was always angry at defaut `Command Prompt`. After some searching here and there, I found excellent [Cmder](http://cmder.net/). 

These days, Git is everywhere and there is a [Git for Windows](https://git-scm.com/download/win) which installs Git Bash.
Git Bash is a package which contains Unix tools such as `awk`, `cat`, `curl`, ... compiled against Windows API. You can find whole list of them in `c:\Program Files\Git\usr\bin\`

I thought it'd be excellent to start `Cmder` with Git Bash by default, starting in my favorite directory and enjoy Unix tools out of the box. 

Here is the result:

I created new task called `git bash`, added _Task parameters_: `/icon "c:\Program Files\Git\mingw64\share\git\git-for-windows.ico"`, added _Command_: `"c:\Program Files\Git\bin\sh.exe" --login -i` and clicked _Startup dir..._ button and navigated to my desired startup directory what resulted into `-new_console:d:C:\dev\eit` being prepended in front of command.

`sh.exe` parameters are actually `bash` parameters, see [man bash](https://linux.die.net/man/1/bash)
* `--login` = Make bash act as if it had been invoked as a login shell
* `-i` = the shell is interactive

![Git Bash task in Cmder](cmder-task-snip.PNG)

I also set git bash task as `Startup` task to run automatically on `Cmder` startup:

![Startup task in Cmder](cmder-startup-snip.PNG)

Enjoy in the same way as I do ;)
