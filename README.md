# Update command scripts

Want to update your computer software? The update command is for you.

When you run `update` the command will run many software updates and upgrades:

  * Linux: Ubuntu `apt`, RedHat `yum`, Arch `yay`, Fedora `dnf`, etc.
  * macOS: `softwareupdate`, Homebrew `brew`, Mac App Store `mas`, etc.
  * tooling: Node `npm`, Python `pip`, Rust `cargo`, Ruby `gem`, Atom `apm`, etc.
  * source code management: `git pull`, `hg pull`, etc.
  * any of your own custom scripts, before and after everything else.


## Install

Clone the repo to your own system:

    $ git clone https://github.com/UpdateCommand/update.git ~/update

Add the `bin` directory to your own path:

    $ export PATH="$PATH:~/update/bin"

Copy the `config` directory to your own directory:

    $ cp -R ~/update/config/update ~/.config/update

Run the script:

    $ update


## What's included

This project has Unix update scripts for many tools,
systems, package managers, language modules, et. al.

 * [`update`](bin/update): run all the udpate scripts.
 * [`update-apm`](bin/update-apm): update Atom Package Manager - for the GitHub Atom editor.
 * [`update-apt`](bin/update-apt): update apt-get - for Debian, Ubuntu, etc.
 * [`update-asdf`](bin/update-apm): update asdf - for managing multiple runtimes and languages.
 * [`update-brew`](bin/update-brew): update Homebrew packages - for macOS.
 * [`update-brewfile`](bin/update-brewfile): update brew packages for macOS by using a Brewfile
 * [`update-brew-cask`](bin/update-brew-cask): update Homebrew Cask packages - for macOS apps.
 * [`update-cabal`](bin/update-cabal): update Haskell Cabal pacakages.
 * [`update-cargo`](bin/update-cargo): update Rust cargo package manager.
 * [`update-cargo-toml`](bin/update-cargo-toml): update Rust cargo package manager Cargo.toml file.
 * [`update-carthage`](bin/update-carthane): udpate Xcode Carthage pacakges - for macOS.
 * [`update-dnf`](bin/update-dnf): update DNF - for Fedora Linux.
 * [`update-hg-pull`](bin/update-hg-pull): update mercurial repositories.
 * [`update-gem`](bin/update-gem): update Ruby gems.
 * [`update-git-pull`](bin/update-git-pull): update git repositories.
 * [`update-gemfile`](bin/update-gemfile): update gem packages for Ruby by using a Gemfile.
 * [`update-mas`](bin/update-mas): update mas packages by using the Mac App Store.
 * [`update-motion`](bin/update-motion): update Ruby Motion - needs a valid paid license.
 * [`update-npm-global`](bin/update-npm-global): update Node Package Manager via global settings.
 * [`update-npm-local`](bin/update-npm-global): update Node Package Manager via local settings.
 * [`update-npm-n-stable`](bin/update-npm-global): update Node Package Manager via `n` environment manager.
 * [`update-macos`](bin/update-macos): update the macOS Mac operating system - large downloads.
 * [`update-pacman`](bin/update-pacman): update pacman - for Arch Linux.
 * [`update-pip`](bin/update-pip): update Python PIP.
 * [`update-pod`](bin/update-pod): update Cocoapods for macOS
 * [`update-podfile`](bin/update-podfile): update Cocoapods packages for macOS by using a Podfile
 * [`update-repos`](bin/update-repos): update Git repositories - customize this for your system.
 * [`update-rustup`](bin/update-rustup): update Rust programming language tooling.
 * [`update-rustup-cargo-test-build-release`](bin/update-rustup-rustup-cargo-test-build-release): update Rust project for release.
 * [`update-run-first`](bin/update-run-first): run custom scripts first, before other commands.
 * [`update-run-last`](bin/update-run-last): run custom scripts last, after other commands.
 * [`update-swift`](bin/update-swift): update macOS Swift language - this merely prints advice.
 * [`update-ubuntu-release`](bin/update-ubuntu-release): update Ubuntu release - for major system upgrades.
 * [`update-yay`](bin/update-yay): update Yay package manager - for Arch Linux
 * [`update-zypper`](bin/update-zypper): update Zypper package manager - for openSUSE

We welcome additions to these scripts.


## Configuration

The command uses a config home directory and program subdirectory:

    ~/.config/update

You can change the config home directory by setting the environment variable `XDG_CONFIG_HOME`. This is POSIX standard. The default is `$HOME/.config/`.


### Run your own scripts first and last

You can configure your own scripts to run first before the start of the update commands, or last after the finish of the update commands.

Put your own scripts in these directories:

    ~/.config/update/update-run-first
    ~/.config/update/update-run-last

For advanced users:

  * You can use as many files and subdirectories as you like.

  * The program runs the user-executable files, and skips the non-user-executable files.


## Package manager files

The program also reads these package manager files:

    ~/.config/Brewfile/Brewfile
    ~/.config/Gemfile/Gemfile
    ~/.config/Podfile/Podfile


### Source code management directories

You can configure the source code management directories to update.

Edit the files in these directories:

    ~/.config/update/update-git-pull/directories
    ~/.config/update/update-hg-pull/directories

For example edit the git pull directories default file:

    ~/.config/update/update-git-pull/directories

The default file currently has these:

    ~/.config/bash
    ~/.config/emacs
    ~/.config/fish
    ~/.config/tmux
    ~/.config/vim
    ~/.config/zsh
    ~/.emacs.d
    ~/.oh-my-zsh
    ~/.tmux
    ~/.vim.d
    ~/.zshrc

For advanced users:

  * You can use as many files and subdirectories as you like.

  * The program updates the existing directories, and skips the non-existing directories.


## To run daily

To run the update command daily, you can use the `crontab` command.

To see if you have an existing `crontab` file, you can list it by running this:

    crontab -l > ~/.crontab

Edit the `~/.crontab` file.

Add a line that runs the `nice` command and use the full path to the `update` command:

    @daily /usr/bin/nice /foo/bar/update

Then install the file:

    crontab ~/.crontab


## Tracking

  * Package: UpdateCommand
  * Version: 6.3.0
  * Created: 2005-07-05
  * Updated: 2021-01-21T07:23:03Z
  * License: GPL-2.0-only
  * Contact: Joel Parker Henderson (https://joelparkerhenderson.com)
