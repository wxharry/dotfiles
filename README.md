# dotfiles

My dotfiles settings. zsh+oh-my-zsh+tmux+vim.



## Prerequisite

* vim
* tmux
* zsh
* oh-my-zsh
* p10k

## Installation
```
git clone https://github.com/wxharry/dotfiles.git && cd dotfiles && ./install
```

## Windows Terminal

### Windows(WSL)
* Windows Terminal (recommended)
* cmd 
* powershell

### Theme
You can pick up one theme on [windows terminal themes](https://windowsterminalthemes.dev/). By clicking the `get theme` button below, you could easily copy and paste the theme to the `settings.json` in Windows Terminal. (I am currently using `Relaxed`)



## Shell

I am currently using [zsh](https://www.zsh.org/).

I also installed [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh) to manage my zsh configuration. oh-my-zsh have a lot of themes, you can pick one in [Themes in ohmyzsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes).

The theme I am currently using is  [powerlevel10k](https://github.com/romkatv/powerlevel10k) and I highly recommend it. p10k is easy to install and configure. 

### Tips

1. Edit `.zshrc` to configure zsh by omz.

2. After editing `.zshrc`, use `source ~/.zshrc` to update zsh. 



## Tmux

I mixed some of tmux theme schemes and self-made this style. 

I installed [tpm](https://github.com/tmux-plugins/tpm) as my tmux plugin manager.

All the plugins are in `tmux/.tmux/plugin`.

I want to keep my dotfile simple, so there are only a few plugins. 

### Tips

1. Default color in tmux is 8 colors. You could use `echo $TERM` to see the difference. 

   You need to edit `.tmux.conf` to change default terminal to 256.

2. After editing `.tmux.conf`, use `tmux source .tmux.conf` to update tmux.



## vim

I am using the default color scheme in vim. (I tried to add and change color schemes, but the default one fit the best.)

I installed [vim-plug](https://github.com/junegunn/vim-plug) to manage vim plugins. 

All the vim plugins are in `vim/.vim/plugged`. Color schemes can either be installed as a plugin with vim-plug or download to `vim/.vim/colors`.


## To do

[See details](https://github.com/wxharry/dotfiles/projects/1)



## Screenshots

![Snipaste_2021-06-28_23-10-11](https://user-images.githubusercontent.com/39271899/123660402-35742500-d866-11eb-8975-d96571820f3f.png)



![Snipaste_2021-06-26_idk](https://user-images.githubusercontent.com/39271899/123531238-90f2c580-d735-11eb-9dcc-84d4fdfdc959.jpg)



![Snipaste_2021-06-26_22-37-18](https://user-images.githubusercontent.com/39271899/123531206-407b6800-d735-11eb-9cca-b28eb7d84281.png)
