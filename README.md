# dotfiles


Steps to setup environment in new machine
-----------------------------------------


1. git clone git@github.com:perezbecker/dotfiles.git in home directory  
2. Run makesymlinks.sh command
3. Check files dotfiles_old directory to see if previous dotfiles existed and copy useful information into this repo. Delete dotfiles_old when done.
4. install Tmux
5. Remap Capslock to Control + Escape
   On Linux use xcape and follow these instructions: 
   http://www.economyofeffort.com/2014/08/11/beyond-ctrl-remap-make-that-caps-lock-key-useful/
            
   Note that the following lines need to be added to ~/.profile or ~/.bashrc (adding to .profile made it crash)
   setxkbmap -option 'caps:ctrl_modifier'
   xcape -e 'Caps_Lock=Escape'
6. Cretate directory ~/dotfiles/vim/bundle
7. Clone Vundle.vim (Vim bundle manager) into directory ~/dotfiles/vim/bundle by running "git clone https://github.com/VundleVim/Vundle.vim.git" 
8. Install all plugins handled by Vundle by running :PluginInstall inside a vim session.
9. Softlink vid command to ~/bin/

Intersting Websites
-------------------

http://jilles.me/badassify-your-terminal-and-shell/
https://github.com/christoomey/dotfiles

