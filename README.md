# SixArm.com » Unix » <br> Update scripts for sysops

This repo has Unix update scripts to help a sysop update various
operating systems, package managers, language modules, et. al.

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
 * `update-repos`: update Git repositories - customize this for your system.
 * `update-ubuntu-release`: update Ubuntu release - for major Linux system upgrades.


## Run  hourly

To run the update command daily, you can use the `crontab` command.

To see if you have an existing `crontab` file, you can list it by running this:

    crontab -l > ~/.crontab

Edit the `~/.crontab` file.

Add a line that runs the `nice` command and use the full path to the `update` command:

    @hourly /usr/bin/nice /foo/bar/update

Then install the file:

    crontab ~/.crontab
2015-08-09


## Tracking

  * Package: UpdateCommand
  * Version: 4.1.0
  * Created: 2005-07-05
  * Updated: 2016-11-11
  * License: GPL
  * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)

