# PDE-starter

Bootstrap scripts for setting up [Neovim](https://neovim.io/)-based PDE([Personalized Development Environment](https://youtu.be/QMVIJhC9Veg?si=VgJQLBVTIYmNjVSD)).

**No root permissions are required, and the setup has minimal impact on local dependencies.**

The following tools will be installed:

- [bat](https://github.com/sharkdp/bat)
- [delta](https://github.com/dandavison/delta)
- [difftastic](https://github.com/Wilfred/difftastic)
- [fd](https://github.com/sharkdp/fd)
- [fzf](https://github.com/junegunn/fzf)
- [fw](https://github.com/yilinfang/fw)
- [Lazygit](https://github.com/jesseduffield/lazygit)
- [Lsd](https://github.com/lsd-rs/lsd)
- [Neovim](https://neovim.io/)
- [Node.js](https://nodejs.org/) (required for many plugins and language servers)
- [ripgrep](https://github.com/BurntSushi/ripgrep)
- [SAD!](https://github.com/ms-jpq/sad)
- [Tmux](https://github.com/tmux/tmux)
- [Yazi](https://github.com/sxyazi/yazi)
- [Zellij](https://zellij.dev/)
- [Zoxide](https://github.com/ajeetdsouza/zoxide)

The following configurations will be set up:

- [Neovim](https://github.com/yilinfang/nvim)
- [Tmux](https://github.com/yilinfang/tmux)

Please refer to the scripts for detailed installation instructions.

**Important:** Make sure to back up your existing configurations for Neovim, tmux, and other tools before running the scripts.

## Requirements

- Git >= 2.19.0
- curl
- Xcode Command Line Tools (MacOS only, for building tmux)

## Motivation

I enjoy coding with my PDE includes Neovim and other useful tools (such as ripgrep, fd, bat and Lazygit) on my Mac. With Homebrew, I can easily manage these dependencies.

However, I came across following issues:

1. I do a lot of development on remote servers, and I often need to set up my PDE from scratch. I do not have root permission on some of these servers, and some package in the repositories are outdated or unavailable.
2. On my local Mac, I used to use Homebrew to manage my PDE's dependencies. However, I find that Homebrew does not allowed me to install a specific version of a package which may caused breaks, as many of the tools are not in stable stage and they are developed rapidly.

To solve these issues, I decided to create a set of scripts that can help me set up my PDE quickly and easily. The scripts will install the dependencies in a local directory, and they will not interfere with the system's package manager.

_**Note #1**: Tmux does not provide a pre-built binary. For linux, I provide a static built binary, you can check how it is built or build on you own [there](https://github.com/yilinfang/static-tmux-builder). For MacOS, static builds are not supported, I use a script to build tmux, you can check the script [there](https://github.com/yilinfang/tmux-macos-builder)._

_**Note #2**: Git and curl are not included because they are usually pre-installed and ready-to-use on most servers I use.:D_

## Uninstallation

1. Run `cleanup-config-unix.sh` to remove the configurations.
2. Delete the `~/.pde` directory.
3. Remove any `pde-starter` related entries in `config.fish` or `.bashrc`.
