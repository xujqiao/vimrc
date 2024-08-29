camxu's config file
===============


# VIM

## Bundle Plugins

* [Vundle][vundle] - an excellent vim plugin management tool
* [Surround][surround] - quoting/parenthesizing made simple
* [NerdTree][nerdTree] - tree explorer files plugin
* [Airline][airline] - great status plugin
* [Tagbar][tagbar] - tagbar
* [EasyMotion][easyMotion] - very useful search tools like the plugin [Vimium][vimium] in Chrome
* [AutoClose][autoClose] - pair of <> () [] {} and so on
* [A][a] - switch between .h and .cpp
* [Ack][ack] - ack2
* [Bufferline][bufferline] - buffers in airline
* [Fzf][fzf] - fuzzy search finder
* [Git][git] - fugitive
* [Seoul256][seoul256] - seoul256 color
* [YCM][ycm] -- YouCompleteMe

## Install

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

* `ctags`

```bash
sudo yum install ctags
```


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

* `fzf`

```bash
git clone --depth 1 https://github.com/junegunn/fzf.git
./fzf/install
source ~/.bashrc
```

* `ycm`

```bash
# 1. upgrade vim with py3
git clone https://github.com/vim/vim
cd vim;
# 要打开 vim 的 python3 支持
./configure --enable-python3interp=yes --prefix=xxxx
make install -j16

# 2. download clangd binary file
visit https://github.com/clangd/clangd/releases/latest get latest binary
unzip to /path/to/clangd

# 3. vim PluginInstall

# 4. install ycm with clangd
cd ~/.vim/bundle/YouCompleteMe
./install.py --clangd-completer
```

5. Install the Plugins

```bash
vim
:PluginInstall
```

## Key Bindings

* leader + p -> search local files
* leader + f -> search contents with ack
* ctrl + b -> switch next buffer
* ctrl + n -> switch preview buffer


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
[ycm]: https://github.com/ycm-core/YouCompleteMe "ycm"
[vimium]: https://chrome.google.com/webstore/search/vimium?utm_source=chrome-ntp-icon "vimium"


# Zsh

## Plugins

* [Fzf-Tab][fzf-tab] - Replace zsh's default completion selection menu with fzf!
* [Zsh-Syntax-Highlighting][zsh-syntax-highlighting] - Fish shell-like syntax highlighting for Zsh.
* [Zsh-Autosuggestions][zsh-autosuggestions] - Fish-like fast/unobtrusive autosuggestions for zsh.

## Install

1. install zsh and oh-my-zsh

...

2. install plugins

```bash
# fzf-tab
git clone https://github.com/Aloxaf/fzf-tab ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/fzf-tab

# zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# 在.zshrc中plugins里添加括号内的插件
plugins=(git fzf-tab zsh-syntax-highlighting zsh-autosuggestions)
```

[fzf-tab]: https://github.com/Aloxaf/fzf-tab "fzf-tab"
[zsh-syntax-highlighting]: https://github.com/zsh-users/zsh-syntax-highlighting "zsh-syntax-highlighting"
[zsh-autosuggestions]: https://github.com/zsh-users/zsh-autosuggestions "zsh-autosuggestions"

# Tmux

## Install

```bash
ln -s ${HOME}/.vim/tmux.conf ${HOME}/.tmux.conf
```


===============
## Bonus

1. Fuzzy Search Finder

* usage

```bash
# cd
cd **<tab>
<directory name>
```

![screenshot][fuzzy_search_cd]


[fuzzy_search_cd]: https://github.com/xujqiao/vimrc/raw/master/img/fuzzy_search_cd.gif "fuzzy_search_cd.gif"
