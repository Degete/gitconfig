![Git](git.png)

# Gitconfig

## Installation:

```sh
cd ~
git clone --recursive git@github.com:degete/gitconfig.git ~/.git
ln -s .git/gitconfig .gitconfig
cp .git/gitconfig.local .gitconfig.local
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
ssh-add --apple-use-keychain ~/.ssh/<id_ed25519>
```

> The --apple-use-keychain option stores the passphrase in your keychain for you when you add an SSH key to the ssh-agent. If you chose not to add a passphrase to your key, run the command without the --apple-use-keychain option.