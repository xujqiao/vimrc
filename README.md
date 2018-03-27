jxuao's VIM config file
===============


## Bundle Plugins

* [Vundle][vundle] - an excellent vim plugin management tool
* [Surround][surround] - quoting/parenthesizing made simple
* [NerdTree][nerdTree] - tree explorer files plugin
* [Taglist][taglist] - taglist
* [Airline][airline] - great status plugin
* [MultipleCursor][multipleCursor] - select the same parts like sublime Ctrl+D
* [EasyMotion][easyMotion] - very useful search tools like the plugin [Vimium][vimium] in Chrome
* [AutoClose][autoClose] - pair of <> () [] {} and so on
* [A][a] - switch between .h and .cpp
* [Tagbar][tagbar] - tagbar
* [Ctrlp][ctrlp] - search file from project
* [Ack][ack] - ack2

## Themes

* [Solarized][solarized] - very very beautiful color scheme

## Installation (ubuntu)

Backup your own vim files
    
    mv ~/.vim/ ~/.vim.bak/

Clone this repository

    git clone https://github.com/xujqiao/vimrc.git ~/.vim
    git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim

Create link for vimrc, vimrc.local

    ln -s ~/.vim/vimrc.local ~/.vim/vimrc

Dependency

    sudo apt-get install ctags

    // ag https://geoff.greer.fm/ag/
    wget -c https://geoff.greer.fm/ag/releases/the_silver_searcher-2.1.0.tar.gz
    tar -xzvf the_silver_searcher-2.1.0.tar.gz
    cd the_silver_searcher-2.1.0/
    ./configure
    make
    sudo make install

Install the Plugins

    vim
    :PluginInstall

## Key Bindings

* F5 -> Toggle NerdTree file viewer
* F4 -> Toggle Taglist
* F8 -> Toggle Tagbar
* <leader>w -> find word
* <leader>L -> jump to line
* ctrl + p -> search files
* ctrl + f -> search contents with ack

## Bonus

* Fix the incorrect display in vim when setting scheme solarized in vim
    
    1.  Lanch the terminal(Ctrl+Alt+t)
    2.  In the menu, **Edit->Profile Preferences->Colors**. Unchecked the '**Use colors from system theme**' and select one item you like in '**Built-in schemes**', just below previous menu
    3.  Click **Close** button
    4.  Type '**vim**' and enjoy the solarized:)

* If you want to use the taglist to see the structure of your file. You need to run this command in your directory, which is 'ctags -R'. Then open a file in vim and press F4, you can see them.





 [solarized]: http://ethanschoonover.com/solarized "solarized"

 [vundle]: https://github.com/gmarik/Vundle.vim "vundle"
 [surround]: https://github.com/tpope/vim-surround "surround"
 [nerdTree]: https://github.com/scrooloose/nerdtree "nerdTree"
 [taglist]: https://github.com/vim-scripts/taglist.vim "taglist"
 [airline]: https://github.com/bling/vim-airline "airline"
 [multipleCursor]: https://github.com/terryma/vim-multiple-cursors "multiple-cursors"
 [easyMotion]: https://github.com/Lokaltog/vim-easymotion "easyMotion"
 [autoClose]: https://github.com/Townk/vim-autoclose "autoClose"
 [a]: https://github.com/vim-scripts/a.vim "a.vim"
 [tagbar]: https://github.com/majutsushi/tagbar "tagbar"
 [ctrlp]: https://github.com/kien/ctrlp.vim "ctrlp.vim"
 [ack]: https://github.com/mileszs/ack.vim "ack.vim"

 [vimium]: https://chrome.google.com/webstore/search/vimium?utm_source=chrome-ntp-icon "vimium"
