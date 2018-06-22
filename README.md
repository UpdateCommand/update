# Update command scripts

Want to update your computer software? The update command is for you.

When you run `update` the command will run many software updates and upgrades:

  * macOS: `softwareupdate`, Homebrew `brew`, Mac App Store `mas`, etc.
  * Linux: Ubuntu `apt`, RedHat `yum`, Arch `pacman`, Fedora `dnf`, etc.
  * tooling: Node `npm`, Python `pip`, Rust `cargo`, Ruby `gem`, Atom `apm`, etc.


## Install

Clone the rep:

    $ git clone https://github.com/UpdateCommand/update.git

Add the commands to your path as you like:

    $ export PATH="$PATH:~/update/bin"

Run the script:

    $ update

Adjust the scripts as you like:

  * You may freely add or remove any of the scripts.

  * You may freely edit any of the scripts to match your security preferences.


## What's included

This project has Unix update scripts for many tools,
systems, package managers, language modules, et. al.

 * `update`: run all the udpate scripts.
 * `update-apm`: update Atom Package Manager - for the GitHub Atom editor.
 * `update-apt`: update apt-get - for Debian, Ubuntu, etc.
 * `update-brew`: update Homebrew packages - for macOS.
 * `update-brewfile`: update brew packages for macOS by using a Brewfile
 * `update-brew-cask`: update Homebrew Cask packages - for macOS apps.
 * `update-cabal`: update Haskell Cabal pacakages.
 * `update-cargo`: update Rust cargo package manager.
 * `update-cargo-toml`: update Rust cargo package manager Cargo.toml file.
 * `update-carthage`: udpate Xcode Carthage pacakges - for macOS.
 * `update-dnf`: update DNF - for Fedora Linux.
 * `update-gem`: update Ruby gems.
 * `update-gemfile`: update gem packages for Ruby by using a Gemfile.
 * `update-mas`: update mas packages by using the Mac App Store.
 * `update-motion`: update Ruby Motion - needs a valid paid license.
 * `update-npm`: update Node Package Manager.
 * `update-macos`: update the macOS Mac operating system - large downloads.
 * `update-pacman`: update pacman - for Arch Linux.
 * `update-pip`: update Python PIP.
 * `update-pod`: update Cocoapods for macOS
 * `update-podfile`: update Cocoapods packages for macOS by using a Podfile
 * `update-repos`: update Git repositories - customize this for your system.
 * `update-rustup`: update Rust programming language tooling.
 * `update-swift`: update macOS Swift language - this merely prints advice.
 * `update-ubuntu-release`: update Ubuntu release - for major Linux system upgrades.


## To run daily

To run the update command daily, you can use the `crontab` command.

To see if you have an existing `crontab` file, you can list it by running this:

    crontab -l > ~/.crontab

Edit the `~/.crontab` file.

Add a line that runs the `nice` command and use the full path to the `update` command:

    @daily /usr/bin/nice /foo/bar/update

Then install the file:

    crontab ~/.crontab


## Configuration files

This tool will also use any of these configuration files:

    ~/.config/Brewfile/Brewfile
    ~/.config/Gemfile/Gemfile
    ~/.config/Podfile/Podfile

The config directory uses the `XDG_CONFIG_HOME` environment variable, which is a POSIX standard environment variable. The default is `$HOME/.config`.


## Tracking

  * Package: UpdateCommand
  * Version: 5.0.0
  * Created: 2005-07-05
  * Updated: 2018-06-22
  * License: GPL
  * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
