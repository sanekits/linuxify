# Using `linuxify` with [shellkit](https://github.com/sanekits/shellkit-pm#setup)

Shellkit tools expect to find a bash+GNU shell environment and will malfunction in annoying ways on a default Mac shell of `zsh` and `BSD` tools.   To solve this, you can install Linuxify first -- it turns your shell into something more closely resembling a Linux environment.

## How:
0. If you have already installed any shellkits, comment out the `source ~/.local/bin/shellkit-loader.bashrc` line from your `.profile`,`.bashrc` or `.bash_profile`
1. Follow the [Linuxify install instructions below](#install).
2. In your `bash` initialization, be sure that `~/.linuxify` is sourced *before* `~/.local/bin/shellkit-loader.bashrc`
3. **Enjoy!**  Everything seems to just work.  But  **worry!**  You're swapping out the system tools and nobody can guarantee that this will never be a problem.   But **don't worry**: if you ever need a plain-old default Mac `bash` environment, you can do `/bin/bash --norc` and you'll get all the clunky old Mac bash defaults.


# Linuxify

Transparently transform the macOS CLI into a fresh GNU/Linux CLI experience by

- installing missing GNU programs
- updating outdated GNU programs
- replacing pre-installed BSD programs with their preferred GNU implementation
- installing other programs common among popular GNU/Linux distributions

You should review the script, but if you want to go back you can uninstall just
as easily as the install.

## Install

```bash
git clone https://github.com/sanekits/linuxify.git
cd linuxify/
./linuxify install
```

## Uninstall

```bash
./linuxify uninstall
```
