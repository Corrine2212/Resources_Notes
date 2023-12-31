# Terminal Shortcuts

|Operation|Command|
|---|---|
|"home” directory|~ Tilde|
|command to check where you are|pwd Print Working Directory|
|see what you have in the directory|ls|
|‘l’ for long version, gives extra info. e.g. size of file or who has access|ls -l|
|'a’ for all files, displays hidden files and directories. hidden files start with ‘.’|ls -a|
|long version of the list of files|ls -al|
|create a new directory|mkdir|
|change directory|cd|
|move back up one level in the directory|cd ..|
|shortcut to home directory|cd ~ or cd|
|create new file - you can create multiple files: e.g. a_ruby_file.rb another_file.rb|touch|
|move files and rename files e.g. mv a_ruby_file.rb, pre_coursework, mv a_ruby_file.rb ruby_stuff.rb|mv|
|remove files|rm|
|remove directory only when EMPTY|rmdir|


### Other Resources:  
- [A-Z Index of the **Apple macOS** command line](https://ss64.com/osx/)

- [Terminal cheatsheet](https://github.com/0nn0/terminal-mac-cheatsheet) 


**Dock spacer**   
defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="small-spacer-tile";}' && killall Dock

**Mail - remove inline attachments**   
defaults write com.apple.mail DisableInlineAttachmentViewing -bool no