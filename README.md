# dotfiles

Personal dotfiles managed with [chezmoi](https://www.chezmoi.io/). zsh + oh-my-zsh + tmux + vim.

## Bootstrap a new machine

```sh
# 1. Install chezmoi (mac)
brew install chezmoi

# 2. Pull and apply this repo
chezmoi init --apply https://github.com/wxharry/dotfiles.git
```

Or chezmoi-less one-liner:

```sh
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply wxharry
```

By default chezmoi clones into `~/.local/share/chezmoi`. If you prefer keeping the working copy elsewhere (e.g. `~/Code/dotfiles`), set:

```toml
# ~/.config/chezmoi/chezmoi.toml
sourceDir = "/Users/you/Code/dotfiles"
```

## Plugin managers (one-time per machine)

chezmoi only manages config files. Plugin managers and plugins live outside the repo.

```sh
# oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# powerlevel10k
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git \
  ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

# tpm (tmux plugin manager)
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
# then inside tmux: prefix + I  to install configured plugins

# vim plugins (vim-plug is vendored at ~/.vim/autoload/plug.vim)
vim +PlugInstall +qall
```

## Daily workflow

```sh
chezmoi edit ~/.zshrc      # edit source
chezmoi diff               # preview pending changes
chezmoi apply              # apply
chezmoi cd                 # cd into source repo
```

## Machine-local config

Put work-only or machine-specific aliases / env vars in `~/.zshrc.local`. It is sourced by `~/.zshrc` if present and is NOT tracked in this repo. Secrets, AWS profiles, internal hostnames belong here.

## Layout

```
dot_zshrc.tmpl              # zsh config (template — supports {{ .chezmoi.os }} branches)
dot_p10k.zsh                # powerlevel10k theme config
dot_tmux.conf               # tmux config
dot_vimrc                   # vim config
dot_vim/autoload/plug.vim   # vim-plug bootstrap
dot_vim/colors/             # vim color schemes
.chezmoiignore              # files chezmoi skips
```

`dot_` prefix → `.` on apply. `.tmpl` suffix → rendered as Go template.

## Tips

- Edit `dot_tmux.conf`, `chezmoi apply`, then in tmux: `prefix + r` (or `tmux source ~/.tmux.conf`).
- Edit `dot_zshrc.tmpl`, `chezmoi apply`, then `source ~/.zshrc`.
- OS-specific blocks in `dot_zshrc.tmpl`:
  ```
  {{- if eq .chezmoi.os "darwin" }}
  # mac-only
  {{- else if eq .chezmoi.os "linux" }}
  # linux-only
  {{- end }}
  ```
