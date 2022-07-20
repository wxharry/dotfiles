# dotfiles

My dotfiles settings. zsh+oh-my-zsh+tmux+vim.

## Screenshots

![Snipaste_2022-07-20_14-56-51](https://user-images.githubusercontent.com/39271899/180076060-fe9502b8-67b9-4179-88fc-39633cd36994.png)

![Snipaste_2022-07-20_16-32-46](https://user-images.githubusercontent.com/39271899/180076314-16024c38-d8f9-4da3-970d-311fbd9ebaf6.png)


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


## Theme (Windows Terminal)
You can pick up a theme at [windows terminal themes](https://windowsterminalthemes.dev/). Click the `get theme` button below to copy the style and paste it to the `settings.json` in Windows Terminal. (currently using `BlulocoDark`)


## Shell

Currently using [zsh](https://www.zsh.org/).

Installed [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh) to manage my zsh configuration. oh-my-zsh have a lot of themes, you can pick a style you like in [Themes in ohmyzsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes).

I am using [powerlevel10k](https://github.com/romkatv/powerlevel10k) and highly recommend it. It is easy to install and configure. 

### Tips

1. Edit `.zshrc` to configure zsh by omz.

2. After editing `.zshrc`, use `source ~/.zshrc` to update zsh. 


## Tmux

Mixed with some of tmux theme schemes and self-made this style. 

Installed [tpm](https://github.com/tmux-plugins/tpm) as my tmux plugin manager.

All the plugins are in `tmux/.tmux/plugin`.

### Tips

1. Default color in tmux is 8 colors. You could use `echo $TERM` to see the difference. 

   You need to edit `.tmux.conf` to change default terminal to 256.

2. After editing `.tmux.conf`, use `tmux source .tmux.conf` to update tmux.



## vim

I am using the default color scheme in vim. 

Installed [vim-plug](https://github.com/junegunn/vim-plug) to manage vim plugins. 

All the vim plugins are in `vim/.vim/plugged`. Color schemes can either be installed as a plugin with vim-plug or download to `vim/.vim/colors`.

Use `PlugInstall!` and `PlugUpdate!` to install and update plugins in vim.


## Trouble Shooting
**no such file or directory: $HOME/.oh-my-zsh/oh-my-zsh.sh**
Install oh-my-zsh
``` bash
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```
**[oh-my-zsh] theme 'powerlevel10k/powerlevel10k' not found**
Install p10k
``` bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

