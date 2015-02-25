# Candy's VIM config file
> Author: Candy Heo

## Bundle Plugins

*   [Vundle][vundle] - an excellent vim plugin management tool
*   [Surround][surround] - quoting/parenthesizing made simple
*   [NerdTree][nerdTree] - tree explorer files plugin

## Themes

*   [Solarized][solarized] - very very beautiful color scheme

## Installation (ubuntu)

Backup your own vim files
    
    mv /etc/vim/vimrc /etc/vim/vimrc.bak
    mv /etc/vim/vimrc.local /etc/vim/vimrc.local.bak
    mv ~/.vim/ ~/.vim.bak/

Clone this repository

    git clone git@github.com:xujqiao/vimrc.git .vim

Create link for vimrc, vimrc.local

    ln -s .vim/vimrc /etc/vim/vimrc
    ln -s .vim/vimrc.local /etc/vim/vimrc.local

Install the Plugins

    vim
    :PluginInstall

## Key Bindings

*   F5 -> Toggle NerdTree file viewer













 [solarized]: http://ethanschoonover.com/solarized "solarized"

 [vundle]: https://github.com/gmarik/Vundle.vim "vundle"
 [surround]: https://github.com/tpope/vim-surround "surround"
 [nerdTree]: https://github.com/scrooloose/nerdtree "nerdTree"
