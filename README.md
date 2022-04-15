camxu's VIM config file
===============


## Bundle Plugins

* [Vundle][vundle] - an excellent vim plugin management tool
* [Surround][surround] - quoting/parenthesizing made simple
* [NerdTree][nerdTree] - tree explorer files plugin
* [Airline][airline] - great status plugin
* [EasyMotion][easyMotion] - very useful search tools like the plugin [Vimium][vimium] in Chrome
* [AutoClose][autoClose] - pair of <> () [] {} and so on
* [A][a] - switch between .h and .cpp
* [Ack][ack] - ack2
* [Bufferline][bufferline] - buffers in airline
* [Fzf][fzf] - fuzzy search finder
* [Git][git] - fugitive
* [Seoul256][seoul256] - seoul256 color

## Installation

1. Backup your own vim files
```bash
mv ~/.vim/ ~/.vim.bak/
```

2. Clone this repository

```bash
git clone https://github.com/xujqiao/vimrc.git ~/.vim
git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

3. Create link for vimrc, vimrc.local

```bash
ln -s ~/.vim/vimrc.local ~/.vim/vimrc
```

4. Install dependency

* `ag`

```bash
// ag https://geoff.greer.fm/ag/
wget -c https://geoff.greer.fm/ag/releases/the_silver_searcher-2.1.0.tar.gz
tar -xzvf the_silver_searcher-2.1.0.tar.gz
cd the_silver_searcher-2.1.0/
sudo yum install -y pcre-devel zlib-devel xz-devel
./configure
make
sudo make install
```

* `fuzzy search finder`

```bash
git clone --depth 1 https://github.com/junegunn/fzf.git
./fzf/install
source ~/.bashrc
```

5. Install the Plugins

```bash
vim
:PluginInstall
```

## Key Bindings

* F5 -> Toggle NerdTree file viewer
* F4 -> Toggle Taglist
* F8 -> Toggle Tagbar
* ctrl + p -> search files
* ctrl + f -> search contents with ack
* ctrl + g -> switch next buffer
* ctrl + n -> switch preview buffer
* ctrl + t -> open terminal

## Bonus

1. Fuzzy Search Finder

* usage

```bash
# cd
cd **<tab>
<input directory or file name>
```

![screenshot][fuzzy_search_cd]


[vundle]: https://github.com/gmarik/Vundle.vim "vundle"
[surround]: https://github.com/tpope/vim-surround "surround"
[nerdTree]: https://github.com/scrooloose/nerdtree "nerdTree"
[airline]: https://github.com/bling/vim-airline "airline"
[easyMotion]: https://github.com/Lokaltog/vim-easymotion "easyMotion"
[autoClose]: https://github.com/Townk/vim-autoclose "autoClose"
[a]: https://github.com/vim-scripts/a.vim "a.vim"
[tagbar]: https://github.com/majutsushi/tagbar "tagbar"
[ack]: https://github.com/mileszs/ack.vim "ack.vim"
[bufferline]: https://github.com/bling/vim-bufferline "vim-bufferline.vim"
[fzf]: https://github.com/junegunn/fzf "fzf"
[git]: https://github.com/tpope/vim-fugitive "git"
[seoul256]: https://github.com/junegunn/seoul256.vim "seoul256"

[vimium]: https://chrome.google.com/webstore/search/vimium?utm_source=chrome-ntp-icon "vimium"
[fuzzy_search_cd]: https://github.com/xujqiao/vimrc/raw/master/img/fuzzy_search_cd.gif "fuzzy_search_cd.gif"

