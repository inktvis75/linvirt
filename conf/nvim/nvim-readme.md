# Neovim

## Requirements

- neovim
- nodejs
- nodejs packages:
  - npm i -g neovim
  - npm i -g yaml-language-server
  - npm i -g bash-language-server
- yearn
- git
- python3
- python packages
  - pyx
  - neovim

## Environment Variable

Edit ~/.bash_profile and add:

```
export XDG_DATA_HOME="~/.config"
```

## Vim-Plug installation

```
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

## Neovim configuration

1. Copy nvim-init to ~/.config/nvim/init.nvim, if needed, change the path to the python3
   executable
2. Start nvim and execute:
   - :PlugInstall
   - :call coc#util#install()
   - :CocInstall coc-yaml
   - :CocInstall coc-sh
   - :CocConfig
3. Paste the content of nvim-coc-settings.json and save
