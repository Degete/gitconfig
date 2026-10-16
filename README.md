<picture>
  <source srcset="./git.svg"/>
  <img
    alt="git logo"
    src="./git.svg"
    height="128px"
    width="128px"
    align="left"
  />
</picture>

### Gitconfig by Degete

> *Git configuration for everyone*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)
[![Open Source](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/degete/gitconfig)

## Getting started

```sh
$ cd ~
$ git clone --recursive git@github.com:degete/gitconfig.git ~/.gitconfig.d
$ ln -s .gitconfig.d/gitconfig .gitconfig
$ cp .gitconfig.d/gitconfig.local .gitconfig.local
```

## Config ssh keys

Modify `~/.ssh/config` file to automatically load keys into the ssh-agent and store passphrases in your keychain.

```sh
Host *
  AddKeysToAgent yes
  UseKeychain yes # If don't use a passphrase, omit this
  IdentityFile ~/.ssh/<id_ed25519>
```

## Add private keys to the ssh-agent

To add the keys and store your passphrase in the keychain:

```sh
$ ssh-add --apple-use-keychain ~/.ssh/<id_ed25519>
```

> The --apple-use-keychain option stores the passphrase in your keychain for you when you add an SSH key to the ssh-agent. If you chose not to add a passphrase to your key, run the command without the --apple-use-keychain option.

## Self Promotion

If you find this project useful, consider giving it a ★ on [GitHub](https://github.com/degete/gitconfig). You can also follow [Degete](https://github.com/degete) for more projects on [GitHub](https://github.com/degete/).

### See also

- [zshrc](https://github.com/degete/zshrc): ⚙️ ZSH config files
- [tmux-conf](https://github.com/degete/tmux-conf): ⚙️ tmux config files
- [vimrc](https://github.com/degete/vimrc): ⚙️ Vim config files
- [nvim-config](https://github.com/degete/nvim-config): ⚙️ Neovim config files
- [brewfile](https://github.com/degete/brewfile): ⚙️ brewfile config file for macOS 🍏

## License

This project is licensed under the [MIT License](./LICENSE).

Copyright (c) David Tort.
