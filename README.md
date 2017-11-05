# dotfiles


Steps to setup environment in new machine
-----------------------------------------


1. git clone git@github.com:perezbecker/dotfiles.git in home directory  
2. Run makesymlinks.sh command
3. install Tmux
4. Remap Capslock to Control + Escape
   On Linux use xcape and follow these instructions: 
   http://www.economyofeffort.com/2014/08/11/beyond-ctrl-remap-make-that-caps-lock-key-useful/
            
   Note that the following lines need to be added to ~/.profile or ~/.bashrc (adding to .profile made it crash)
   setxkbmap -option 'caps:ctrl_modifier'
   xcape -e 'Caps_Lock=Escape'
5. Cretate directory ~/dotfiles/vim/bundle
6. Clone Vundle.vim (Vim bundle manager) into directory ~/dotfiles/vim/bundle by running "git clone https://github.com/VundleVim/Vundle.vim.git" 
7. Install all plugins handled by Vundle by running :PluginInstall inside a vim session.
8. Softlink vid command to ~/bin/
