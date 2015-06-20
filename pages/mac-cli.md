# 常用 CLI 应用

## HomeBrew & HomeBrew Cask

Homebrew 是 Mac 下最好用的包管理器，推荐所有控制台应用都尽可能使用 brew 管理。

安装 [HomeBrew](http://brew.sh)：

```sh
ruby -e “$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)”
```

Homebrew Cask 是 Homebrew 的插件，作为 Homebrew 在 GUI 应用上的补充。

安装 [HomeBrew Cask](https://github.com/caskroom/homebrew-cask)：

```sh
brew install caskroom/cask/brew-cask
```


## zsh & oh-my-zsh!

被称为终极 shell 也没什么问题。Mac 已经预装了 zsh ，只需要安装 `oh-my-zsh!` 即可：

```sh
curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
```

或者：

```sh
wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O - | sh
```

Ubuntu 中需要先注册 zsh 可用：

```sh
command -v zsh | sudo tee -a /etc/shells
chsh -s "$(command -v zsh)" "${USER}"
```

切换 sh 之后可能需要重新登录才能生效。


## tree

显示目录的树状图



## htop

进程管理器，比自带的 top 要强大许多。



## autojump

在常用目录间快速跳转，命令是 `j`。



## IPython

提供更强大的 Python REPL 环境，配合 IPython Notebook 能提供强大的 web 执行环境。



## ag

文件查找命令，类似于 `ack`。


## ncdu

磁盘空间占用分析。


## dos2unix

换行符转换工具（Windows下换行符是 ``\r\n``，OS X 是 ``\n``）


## coreutils

Some missing Linux commands in shell


## mpv-player

```
brew tap mpv-player/mpv
brew install mpv
```


## git

最流行的分布式代码管理工具。Mac 自带了 git ，只需要做一下简单的配置：

```shell
git config --global user.name "Kane Blueriver"
git config --global user.email "kxxoling@gmail.com"
git config --global credential.helper osxkeychain 	# 设置 Mac KeyChain 工具来自动提交 GitHub 验证信息
```

git 教程：[小猫都能学会的 git 教程](http://www.davidrevoy.com/article193/guide-building-krita-on-linux-for-cats)

常用的 git 插件有：

* zsh git 插件
* git-flow（[AVH Edition](https://github.com/petervanderdoes/gitflow) ``brew install git-flow-avh``）
* [legit](https://github.com/kennethreitz/legit)。legit 主要提供 git-flow 的命令封装。

PS：zsh git 插件在较大的项目中会导致启动缓慢，建议在大型项目中关闭该插件。


## pip & gem & npm & cnpm

pip 以外的所有 Python 应用都应该使用 pip 来安装！

gem 是 Ruby 的包管理器，安装 compass / puppet / vagrant 等 Ruby 应用时离不开 gem。

npm 是 node.js 包管理器，cnpm 是 淘宝提供的 npm 替代品。

```
brew install npm
npm install cnpm -g --registry=https://registry.npm.taobao.org 		# 安装 cnpm 来替代 npm 命令
```



## pgcli

[pgcli](https://github.com/amjith/pgcli) 是控制台中的 PostgreSQL 管理工具，功能强大！
推荐使用 brew 安装：

```sh
brew install pgcli
```

不过，由于 pgcli 是 Python 应用，你也可以使用 ``pip`` 或者 ``easy_install`` 安装：

```sh
pip install pgcli
```


## uwsgi & gunicorn

提供 WSGI 支持的 web 服务器。



## sphinx

Python 社区的文档管理标准，著名的文档托管服务 [ReadTheDocs](http://rtfd.org) 服务就是基于其搭建，
支持 i18n，配合 Python 注释自动生成非常方便。



## LiveReload

[LiveReload](https://github.com/lepture/python-livereload) 是使用 Python 开发的自动刷新工具，
可以配合 livereload Chrome 插件使用。

文档：[en](https://github.com/lepture/python-livereload)



## virtualenv

提供 Python 虚拟环境的隔离。



## VirtualEnvWrapper

virtualenv 命令复杂，目录的管理也比较混乱，VirtualEnvWrapper 是在这之上的一层封装。



## tmux

控制台中的标签页管理工具以及分屏管理工具。


## Vim

目前最常用的编辑器是 Vim，配置主要来自胡淼的 [dot-vim](https://github.com/humiaozuzu/dot-vimrc)，
也有一些自己的特别配置。安装：

```sh
mv ~/.vim ~/.vim.orig
mv ~/.vimrc ~/.vimrc.orig
git clone git://github.com/humiaozuzu/dot-vimrc.git ~/.vim
ln -s ~/.vim/vimrc ~/.vimrc
git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
vim +BundleClean +BundleInstall +qall
```


## aria2

[aira2](http://aria2.sourceforge.net/) 是 OS X 和 Linux 下通用的下载工具，可以安装在路由器、NAS 等 Linux 机器上。

配合 [YAAW](https://github.com/binux/yaaw) 或者 [webui-arias2](https://github.com/ziahamza/webui-aria2) 非常方便。

附：
* [aria2 配置示例](http://blog.binux.me/2012/12/aria2-examples/)
* [YAAW](http://binux.github.io/yaaw/)
* [Aria2 & YAAW 使用说明](http://aria2c.com/usage.html)
