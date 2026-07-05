# gcpadder-linux-fork

Lazy Fork that is mostly vibe coded and only changes a few things for my own convenience.<br>
I barely do stuff myself on it due to my lack of C++ knowledge so i let AI do the coding and adjust things personally in post when able to.

TL;DR: If you are against using AI code do not use this.

My own fork of the GCPadder homebrew application can be found [here](https://github.com/TheCraZyDuDee/GCPadder-Fork).

Most notable changes:
- reading and applying IP Address and Port from configuration.
- remapping of B, X, Y and Z for Virtual Controller mapping.
- triggers working properly
- console interface that displays useful information

Userspace Linux driver for the Wii homebrew application [GCPadder](https://github.com/InvoxiPlayGames/GCPadder), originally by [InvoxiPlayGames](https://github.com/InvoxiPlayGames).

Linux Client originally from [TheEssem](https://github.com/TheEssem).

To build this run this in GCC:
```sh
$ g++ -O2 -o gcpadder `pkg-config --cflags libevdev` `pkg-config --libs libevdev` main.cpp -lncurses
```

In fish shell:

```sh
$ g++ -O2 -o gcpadder (pkg-config --cflags libevdev) (pkg-config --libs libevdev) main.cpp -lncurses
```
