jxuao's VIM config file
===============


## Bundle Plugins

* [Vundle][vundle] - an excellent vim plugin management tool
* [Surround][surround] - quoting/parenthesizing made simple
* [NerdTree][nerdTree] - tree explorer files plugin
* [Airline][airline] - great status plugin
* [MultipleCursor][multipleCursor] - select the same parts like sublime Ctrl+D
* [EasyMotion][easyMotion] - very useful search tools like the plugin [Vimium][vimium] in Chrome
* [AutoClose][autoClose] - pair of <> () [] {} and so on
* [A][a] - switch between .h and .cpp
* [Tagbar][tagbar] - tagbar
* [Ctrlp][ctrlp] - search file from project
* [Ack][ack] - ack2
* [Bufferline][bufferline] - buffers in airline

## Installation

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
* \<leader\>w -> find word
* \<leader\>L -> jump to line
* ctrl + p -> search files
* ctrl + f -> search contents with ack
* ctrl + g -> switch next buffer which is previous buffer in airline


[vundle]: https://github.com/gmarik/Vundle.vim "vundle"
[surround]: https://github.com/tpope/vim-surround "surround"
[nerdTree]: https://github.com/scrooloose/nerdtree "nerdTree"
[airline]: https://github.com/bling/vim-airline "airline"
[multipleCursor]: https://github.com/terryma/vim-multiple-cursors "multiple-cursors"
[easyMotion]: https://github.com/Lokaltog/vim-easymotion "easyMotion"
[autoClose]: https://github.com/Townk/vim-autoclose "autoClose"
[a]: https://github.com/vim-scripts/a.vim "a.vim"
[tagbar]: https://github.com/majutsushi/tagbar "tagbar"
[ctrlp]: https://github.com/kien/ctrlp.vim "ctrlp.vim"
[ack]: https://github.com/mileszs/ack.vim "ack.vim"
[bufferline]: https://github.com/bling/vim-bufferline "vim-bufferline.vim"

[vimium]: https://chrome.google.com/webstore/search/vimium?utm_source=chrome-ntp-icon "vimium"
