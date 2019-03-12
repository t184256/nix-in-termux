# NOTICE

I've shifted my efforts to focus on [Nix-on-Droid](https://nix-on-droid.unboiled.info),
a different approach to bringing Nix to Android devices:

* it does not require Termux-the-distro in-between Android and Nix userland;
* it features a standalone app that can coexist with original Termux.

Please consider installing this one to get Nix on your device instead.

Links to the new projects:

* Downloads: https://nix-on-droid.unboiled.info
* Bootstrap script: https://github.com/t184256/nix-on-droid-bootstrap
* App source: https://github.com/t184256/nix-on-droid-app


# README

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
