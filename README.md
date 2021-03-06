# Dotfiles 


## Install

On a fresh installation of macOS:

    sudo softwareupdate -i -a
    xcode-select --install

Install the dotfiles with git:

    git clone https://github.com/crumpetsandtea/dotfiles.git ~/.dotfiles && source ~/.dotfiles/install

Or alternatively, install into `~/.dotfiles` with curl:

    curl -fsSL https://raw.githubusercontent.com/crumpetsandtea/dotfiles/master/install-remote | bash


## Conventions

- **bin/**: Anything in `bin` will get added to your `$PATH` and be made available everywhere.
- **{folder}/{env,alias,functions,path,profile,prompt}**: Any executable file named `env`, `alias`, 
  `functions`, `path`, `profile`, or `env` is loaded into the shell environment.
- **{folder}/\.\***: Any `.dotfiles` get copied into `~`. These get copied when you run `dotfiles files`.
- **{folder}/install**: Any executable named `install` will be run with `dotfiles install`.


## dotfiles help command

    Usage: dotfiles <command>

    Commands:
    -  files     Copies dotfiles (${folder}/.*) to ~ if they don’t already exist
    -  install   Runs all installers (${folder}/install)
    -  macOS     Apply macOS system defaults (requires reboot)
    -  help      This help message
