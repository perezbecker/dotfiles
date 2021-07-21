# dotfiles


Steps to setup environment in new machine
-----------------------------------------


1. Run `git clone git@github.com:perezbecker/dotfiles.git` in home directory of new machine
1. Run `makesymlinks.sh` command
1. Check files dotfiles_old directory to see if previous dotfiles existed and copy useful information into this repo. Delete dotfiles_old when done.
1. install Tmux
1. Remap Capslock to Control + Escape
   On Linux use xcape and follow [these instructions](http://www.economyofeffort.com/2014/08/11/beyond-ctrl-remap-make-that-caps-lock-key-useful/)
   Note that the following lines need to be added to ~/.profile or ~/.bashrc (adding to .profile made it crash)
   ```
   setxkbmap -option 'caps:ctrl_modifier'
   xcape -e 'Caps_Lock=Escape'
   ```
1. Cretate directory `~/dotfiles/vim/bundle`
1. Clone Vundle.vim (Vim bundle manager) into directory `~/dotfiles/vim/bundle` by running `git clone https://github.com/VundleVim/Vundle.vim.git`
1. Install all plugins handled by Vundle by running `:PluginInstall` inside a vim session
1. The vim markdown plugin requires you to run `:call mkdp#util#install()` inside the vim session after PluginInstall. The `github-markdown.css` file is already included in the `other` directory. Run `:MarkdownPreview` in vim to see a preview of the markdown file in a browser. See this [youtube video](https://www.youtube.com/watch?v=22JAs0kNA9k) for details
1. Softlink vid command to ~/bin/

Intersting Websites
-------------------

[Badassify your terminal and shell](http://jilles.me/badassify-your-terminal-and-shell/)</br>
[Chris Toomey's dotfiles](https://github.com/christoomey/dotfiles)

i3 Configuration steps
----------------------

1. Copy fonts in ~/.fonts directory
2. Install rofi: sudo apt intall rofi
3. Install compton: sudo apt install compton
4. Install xcape: sudo apt install xcape
5. Install i3blocks: sudo apt install i3blocks
6. Create simbolic link for i3blocks.conf from ~/dotfiles/i3confguration/i3blocks.conf-laptop/-desktop: ln -s i3blocks.conf-desktop i3blocks.conf
7. Create simbolic link for dpbrofi from ~/dotfiles/i3confguration/dpbrofi-laptop/-desktop: ln -s dpbrofi-desktop dpbrofi
