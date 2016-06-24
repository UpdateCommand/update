# Update command scripts

This project has Unix update scripts for many tools,
systems, package managers, language modules, et. al.

 * `update`: run all the udpate scripts.
 * `update-apm`: Atom Package Manager for the GitHub Atom editor.
 * `update-apt`: apt-get for Debian, Ubuntu, etc.
 * `update-brew`: Homebrew packagesfor OSX.
 * `update-cabal`: Cabal Haskell package manager.
 * `update-carthage`: Carthage for Mac apps and iOS apps.
 * `update-gem`: Ruby gem package manager.
 * `update-motion`: Ruby Motion - needs a valid paid license.
 * `update-npm`: Node Package Manager for JavaScript.
 * `update-oh-my-zsh`: ZSH shell script and plugins.
 * `update-osx`: Mac OSX operating system - very large downloads.
 * `update-pip`: Python PIP package manager.
 * `update-repos`: Git repositories - customize this for your system.
 * `update-ubuntu-release`: Ubuntu Linux OS major upgrades - very large downloads.

## To run hourly

To run the update command daily, you can use the `crontab` command.

To see if you have an existing `crontab` file, you can list it by running this:

    crontab -l > ~/.crontab

Edit the `~/.crontab` file.

Add a line that runs the `nice` command and use the full path to the `update` command:

    @hourly /usr/bin/nice /foo/bar/update

Then install the file:

    crontab ~/.crontab
