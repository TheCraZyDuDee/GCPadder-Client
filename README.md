# gcpadder-linux-fork

Userspace Linux driver for the Wii homebrew application [GCPadder](https://github.com/InvoxiPlayGames/GCPadder), originally by [InvoxiPlayGames](https://github.com/InvoxiPlayGames).

Linux Client originally from [TheEssem](https://github.com/TheEssem).

My own fork of the GCPadder homebrew application can be found [here](https://github.com/TheCraZyDuDee/GCPadder-Fork).

This is a lazy Fork that is mostly vibe coded and only changes a few things for my own convenience.<br>
I barely do stuff myself on it due to my lack of C++ knowledge so i let AI do the coding and adjust things personally in post.

TL;DR: If you are against using AI code do not use this.

Most notable changes:
- pre-configured desktop file for easier usage
- configuration file support
- remapping of B, X, Y and Z for Virtual Controller mapping
- triggers working properly
- console interface that displays useful information

## How to use:

Download the pre-build from [here](https://github.com/TheCraZyDuDee/gcpadder-linux-fork/releases/latest).<br>
Extract and run ```cp -r bin share $HOME/.local``` inside the extracted folder or move files manually.<br>
A new desktop entry will be available named GCPadder Client.

Configuration will be generated on first startup and can be found in $HOME/.config/gcpadder

## Building:

To build this run this in GCC:
```sh
$ g++ -O2 -o gcpadder `pkg-config --cflags libevdev` `pkg-config --libs libevdev` main.cpp -lncurses
```

In fish shell:

```sh
$ g++ -O2 -o gcpadder (pkg-config --cflags libevdev) (pkg-config --libs libevdev) main.cpp -lncurses
```