This script installs Nix package manager inside a Termux installation.
Copyright (c) 2019 Alexander Sosedkin <monk@unboiled.info>

Based off the official Nix install script (https://nixos.org/nix/install),
presumably written by Eelco Dolstra.


This script installs Nix package manager inside a Termux installation.
It does not require root, user namespaces support or disabling SELinux,
but it relies on proot and numerous other hacks instead.
Only tested with aarch64, may also accidentally work on x86.
Sorry, it would not work on 32-bit ARM devices.


Usage:

* Install and run Termux.
* Run `./nix-in-termux` inside Termux to install Nix.
* Run `./nix-in-termux nix something` to run nix subcommands.
* Run `./nix-in-termux nix run nixpkgs.bashInteractive`
  to get a shell with Nix and your Nix user environment.
* Have some quality fun with `nixpkgs`, the vast collection of fine packages
  that is now at your disposal.
* Be careful, as this is carelessly written alpha-quality stuff!

Tips:

* Nothing is installed by default,
  consider getting at least `coreutils` installed.
* Add or switch to a stable channel
  if you want more stable precompiled packages.
