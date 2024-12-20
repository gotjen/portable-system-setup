# System config
`gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'`

## Manually installed APT packages

- APT repo
  - curl
  - flameshot
  - appimagelauncher
  - neofetch
  - terminator
  - python3-pip
    - `[ -e /usr/bin/python ] || sudo ln -s /usr/bin/python3 /usr/bin/python`
  - exa
    - `alias l='exa --icons --group-directories-first`
    - `alias l`
   - zsh
    - `chsh -s /usr/bin/zsh $USER`
   - oh-my-zsh

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.ohmy-zsh/custom}/plugins/zsh-syntax-highlighting
```

  - git
    - `ssh-keygen -t ed25519 -C "hgotjen@gmail.com" -f $HOME/.ssh/[keyname]`
  - ranger
  - nmap
  - neovim
    - `alias vi='nvim'`
  - gnome-shell-extension-manager
    - Awesome Tiles
    - Bing Wallpaper
    - GSConnect
    - NoAnnoyance v2
    - audio output switcher
  - gnome-tweaks
    - Install fonts, apply to system defaults
    - [MesloLG Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.0/Meslo.zip)
  - cura  # 3D Slicing
- GitHub
  - [lazygit](https://github.com/jesseduffield/lazygit)
  - alias lg=lazygit

```bash
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep -Po '"tag_name": "v\K[^"]*')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
tar xf lazygit.tar.gz lazygit
sudo install lazygit /usr/local/bin
```
- Python packages
  - disable "Do you really want to exit ([y]/n)? y"
	  - `ipython create profile`
	  - The config file is located at: `$HOME/.ipython/profile_default/ipython_config.py`
	  - Set `c.TerminalInteractiveShell.confirm_exit = False`
  - ipython
		  - `ipython profile create`
		  - set line 607 `c.TerminalInteractiveShell.confirm_exit = False`
  - numpy, pandas, matplotlib, plotly
- Allow user to use `dmesg`
	- `sudo sysctl kernel.dmesg_restrict=0`
