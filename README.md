# my-one-script-setup

A single shell script to bootstrap a development environment: installs packages, configures Oh My Zsh and the Powerlevel10k theme, adds useful aliases/macros for quality-of-life improvements, and sets up Neovim.

## What it does
- Installs a configurable list of packages (package manager dependent)
- Installs and configures Oh My Zsh
- Installs Powerlevel10k for Zsh prompt theming
- Adds custom aliases and shell macros
- Applies a base Neovim configuration
- Generally intended to get a new machine ready for development quickly

## Aliases & macros (brief)
The script installs a small set of convenience aliases and shell functions to speed up common tasks. Exact names and definitions are in the setup script and the included dotfiles; below are the typical examples included and what they do:
### Aliases:
-  zshcfg: uses nvim to open ~/.zshrc
-  cp, rm, mv: appends -iv to the command
-  mkdir: appends -pv to the command
-  mem: free -h
-  hist: shows the last 20 lines of your zsh hsitory
-  reload: reloads your .zshrc via source
-  omsh: opens ~/.oh-my-zsh in nvim
-  nvcfg: opens ~/.config/nvim/init.lua

### Macros:
-  nv: opens nvim and passes args to nvim
-  mkcd: makes a directory and cd's into it
-  extract: auto extracts several zipped file formats including .zip, .tar, .tar.gz, and .tar.xz 
-  up: equivalent to cd .., can be called with a number to cd backwards by the number, i.e.; up 3 = cd ../../..

## Requirements
- Debain based enviroment 
- POSIX-compatible shell (bash/sh)
- sudo privileges (for system package installation)
- Internet access to download installers and packages
- 
## Quick start
1. Clone the repo:
   git clone https://github.com/hazypugfluff/my-one-script-setup.git
2. Run the script:
   sudo bash setupall.sh
   # or make executable then run:
   # sudo ./setupall.sh

## Customization
- Edit the package list and flags inside the script to match your OS and preferences.
- Change the Neovim and Zsh configuration files in the repo to adjust dotfiles and settings.



## Contributing
Contributions, improvements, and bug reports are welcome. Please open an issue or submit a PR with a brief description of changes.
