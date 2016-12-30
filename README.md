# Update command scripts

This project has Unix update scripts for many tools,
systems, package managers, language modules, et. al.

 * `update`: run all the udpate scripts.
 * `update-apm`: update Atom Package Manager - for the GitHub Atom editor.
 * `update-apt`: update apt-get - for Debian, Ubuntu, etc.
 * `update-brew`: update Homebrew packages - for macOS.
 * `update-brew-cask`: update Homebrew Cask packages - for macOS apps.
 * `update-cabal`: update Haskell Cabal pacakages.
 * `update-carthage`: udpate Xcode Carthage pacakges - for macOS.
 * `update-gem`: update Ruby gems.
 * `update-motion`: update Ruby Motion - needs a valid paid license.
 * `update-npm`: update Node Package Manager.
 * `update-macos`: update the macOS Mac operating system - very large downloads.
 * `update-pip`: update Python PIP.
 * `update-pod`: update a user's default Cocoapods Podfile.
 * `update-repos`: update Git repositories - customize this for your system.
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

This tool looks for these files:

    ~/.config/pod/Podfile



## Tracking

  * Package: UpdateCommand
  * Version: 4.2.0
  * Created: 2005-07-05
  * Updated: 2016-12-29
  * License: GPL
  * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
