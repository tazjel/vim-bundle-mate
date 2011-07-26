# vim-bundle-mate

###introduction
Script to automatically update your scripts in `~/.vim/bundle` directory.
Following a KISS principle there are no external config files. All scripts u need are defined internally - in the update script file.
If you want to use your own plugins, just place them in `bundle/pluginname` dir and do not include plugin name into 'update' file to not to overwrite it while update.
After each plugin install the script will run commands, which you define as an optional parameter. For example: you can cd to command-t directory after install and make the plugin.

####version 1.1:
code refactoring
git clone now uses `--depth=1` option to perform faster download

###prerequisites:
* git  
* vim 7  
* pathogen plugin to vim  
* python 3.2  
* lxml for python 3.2 (python3-lxml in archlinux) - only if you want to receive latest plugin versions  

###usage:
1. edit 'update' file and define plugins u need
2. simply run ./update or python ~/.vim/update

###supported:
1. git repos
2. *.vim and *.zip files on www.vim.org
3. vimball archive (*.vba and *.vba.gz)

###todo:
1. add current downloading plugin version support, so the newest files will not be downloaded again
2. add support for tar, tar.gz archives
3. add support for bzr, mercurial, svn
