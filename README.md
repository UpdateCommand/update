# Update command

Want to update your computer software? The update command can help you.

When you run `update` the command will run many software updates and upgrades.

 * [`update`](bin/update): run all the update scripts.
 * [`update-apm`](bin/update-apm): update Atom Package Manager - for the GitHub Atom editor.
 * [`update-apt`](bin/update-apt): update apt-get - for Debian, Ubuntu, etc.
 * [`update-asdf`](bin/update-apm): update asdf - for managing multiple runtimes and languages.
 * [`update-brew`](bin/update-brew): update Homebrew packages - for macOS.
 * [`update-brewfile`](bin/update-brewfile): update brew packages for macOS by using a Brewfile
 * [`update-brew-cask`](bin/update-brew-cask): update Homebrew Cask packages - for macOS apps.
 * [`update-cabal`](bin/update-cabal): update Haskell Cabal pacakages.
 * [`update-cards`](bin/update-cards): update cards packages - for NuTyX Linux. 
 * [`update-cargo-crate`](bin/update-cargo-crate): update Rust cargo crate project.
 * [`update-cargo`](bin/update-cargo): update Rust cargo package manager.
 * [`update-carthage`](bin/update-carthage): update Xcode Carthage pacakges - for macOS.
 * [`update-choco`](bin/update-choco): update choco Chocolatey packages - for Windows.
 * [`update-dnf`](bin/update-dnf): update DNF - for Fedora Linux.
 * [`update-emerge`](bin/update-emerge): update emerge - for Gentoo Linux.
 * [`update-eopkg`](bin/update-eopkg): update eopkg - for Solus Linux.
 * [`update-flatpak`](bin/update-flatpak): update flatpak - for many Linux distributions.
 * [`update-hg-pull`](bin/update-hg-pull): update mercurial repositories.
 * [`update-gem`](bin/update-gem): update Ruby gems.
 * [`update-git-pull`](bin/update-git-pull): update git repositories.
 * [`update-gemfile`](bin/update-gemfile): update gem packages for Ruby by using a Gemfile.
 * [`update-mas`](bin/update-mas): update mas packages by using the Mac App Store.
 * [`update-motion`](bin/update-motion): update Ruby Motion - needs a valid paid license.
 * [`update-npm-global`](bin/update-npm-global): update Node Package Manager (NPM) via global settings.
 * [`update-npm-local`](bin/update-npm-global): update Node Package Manager (NPM) via local settings.
 * [`update-npm-n-stable`](bin/update-npm-global): update Node Package Manager (NPM) via `n` environment manager.
 * [`update-macos`](bin/update-macos): update the macOS Mac operating system - large downloads.
 * [`update-pacman`](bin/update-pacman): update pacman - for Arch Linux.
 * [`update-pip`](bin/update-pip): update Python PIP.
 * [`update-pnpm-global`](bin/update-pnpm-global): update Performant Node Package Manager (PNPM) via global settings.
 * [`update-pnpm-local`](bin/update-pnpm-global): update Performant Node Package Manager (PNPM) via local settings.
 * [`update-pod`](bin/update-pod): update Cocoapods for macOS
 * [`update-podfile`](bin/update-podfile): update Cocoapods packages for macOS by using a Podfile
 * [`update-repos`](bin/update-repos): update Git repositories - customize this for your system.
 * [`update-rustup`](bin/update-rustup): update Rust programming language tooling.
 * [`update-scoop`](bin/update-scoop): update scoop for system-wide packages - for Windows.
 * [`update-swift`](bin/update-swift): update macOS Swift language - this merely prints advice.
 * [`update-ubuntu-release`](bin/update-ubuntu-release): update Ubuntu release - for major system upgrades.
 * [`update-yay`](bin/update-yay): update Yay package manager - for Arch Linux
 * [`update-yarn`](bin/update-yarn): update Yarn JavaScript packages - for yarn upgrade.
 * [`update-zypper`](bin/update-zypper): update Zypper package manager - for openSUSE


## Install

Clone the repo to your own system, such as:

    $ git clone https://github.com/UpdateCommand/update.git ~/update

Add the `bin` directory to your own path:

    $ export PATH="$PATH:~/update/bin"

Run the script:

    $ update


## Design goals

1. Use POSIX simple shell scripts that developers can customize.

2. Make it easy for developers to help by doing merge requests.

3. Quality is intended for typical developer boxen. YMMV.

We welcome help, and new scripts, and constructive criticism.

If you prefer something more powerful, we highly recommend you consider tools such as Nix and Ansible.


## To run daily

To run the update command daily, you can use the `crontab` command.

To see if you have an existing `crontab` file, you can list it by running this:

    crontab -l > ~/.crontab

Edit the `~/.crontab` file.

Add a line that runs the `nice` command and use the full path to the `update` command:

    @daily /usr/bin/nice /foo/bar/update

Then install the file:

    crontab ~/.crontab


## Special options for package manager files

Some of the update programs can read package manager files:

* `update-brewfile` looks for a `Brewfile` for macOS Homebrew packages.

* `update-gemfile` looks for a `Gemfile` for Ruby gem packages.

* `update-podfile` looks for a `Podfile` for XCode Cocoapod pacakges.

For details, see the respective programs.


### Special options for project manifests

Some of the update programs can read project manifests:

* `update-cargo-crate` looks for `<config>/update-cargo-crate/manifests/*`

* `update-git-pull` looks for `<config>/update-git-pull/manifests/*`

* `update-hg-pull` looks for `<config>/update-hg-pull/manifests/*`

Each manifest file is simply a list of local project directories.

The program skips lines that are comments (begin with #) or blank.

You can use as many manifest files and subdirectories as you like.

For details, see the respective programs.


## Tracking

  * Package: UpdateCommand
  * Version: 7.1.0
  * Created: 2005-07-05
  * Updated: 2023-12-23T19:02:12Z
  * License: GPL-2.0-or-later or contact us for custom
  * Contact: Joel Parker Henderson (https://joelparkerhenderson.com)
