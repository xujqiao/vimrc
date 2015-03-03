# Candy's VIM config file
> Author: Candy Heo

## Bundle Plugins

*   [Vundle][vundle] - an excellent vim plugin management tool
*   [Surround][surround] - quoting/parenthesizing made simple
*   [NerdTree][nerdTree] - tree explorer files plugin
*   [Taglist][taglist] - taglist

## Themes

*   [Solarized][solarized] - very very beautiful color scheme

## Installation (ubuntu)

Backup your own vim files
    
    mv ~/.vim/ ~/.vim.bak/

Clone this repository

    git clone git@github.com:xujqiao/vimrc.git ~/.vim
    git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim

Create link for vimrc, vimrc.local

    ln -s ~/.vim/vimrc.local ~/.vim/vimrc

Install the Plugins

    sudo apt-get install ctags
    vim
    :PluginInstall

## Key Bindings

*   F5 -> Toggle NerdTree file viewer
*   F4 -> Toggle Taglist

## Bonus

*   Fix the incorrect display in vim when setting scheme solarized in vim
    
    1.  Lanch the terminal(Ctrl+Alt+t)
    2.  In the menu, **Edit->Profile Preferences->Colors**. Unchecked the '**Use colors from system theme**' and select one item you like in '**Built-in schemes**', just below previous menu
    3.  Click **Close** button
    4.  Type '**vim**' and enjoy the solarized:)

*   If you want to use the taglist to see the structure of your file. You need to run this command in your directory, which is 'ctags -R'. Then open a file in vim and press F4, you can see them.











 [solarized]: http://ethanschoonover.com/solarized "solarized"

 [vundle]: https://github.com/gmarik/Vundle.vim "vundle"
 [surround]: https://github.com/tpope/vim-surround "surround"
 [nerdTree]: https://github.com/scrooloose/nerdtree "nerdTree"
 [taglist]: https://github.com/vim-scripts/taglist.vim "taglist"
