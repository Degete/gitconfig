![Git](git.png)

# Gitconfig

## Installation:

```sh
cd ~
git clone --recursive git@github.com:degete/gitconfig.git ~/.git
ln -s .git/gitconfig .gitconfig
```

## GPG passphrase on macOS

You might want to have integration to store your keys on the Keychain in macOS, for that install

```sh
brew install pinentry-mac
```

Add the config to `gpg-agent` in order to work with `pinentry-mac`:
```sh
echo "pinentry-program $(which pinentry-mac)" >> ~/.gnupg/gpg-agent.conf
```

Restart `gpg-agent` in order to load the config, and you are ready to go:

```sh
killall gpg-agent
```

To check everything is up, you can execute the command which will ask your passphrase and will allow you to save it on the Keychain.

```sh
echo "Test" | gpg --clearsign
```
