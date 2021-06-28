# dofiles

Dotfiles of my terminal settings


![Snipaste_2021-06-26_idk](https://user-images.githubusercontent.com/39271899/123531238-90f2c580-d735-11eb-9dcc-84d4fdfdc959.jpg)

![Snipaste_2021-06-26_22-37-18](https://user-images.githubusercontent.com/39271899/123531206-407b6800-d735-11eb-9cca-b28eb7d84281.png)


## Terminal

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

### Tips

1. Default color in tmux is 8 colors. You could use `echo $TERM` to see the difference. 

   You need to edit `.tmux.conf` to change default terminal to 256.

2. After editing `.tmux.conf`, use `tmux source .tmux.conf` to update tmux.



## vim
