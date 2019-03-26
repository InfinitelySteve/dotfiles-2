# asdf

```shell
git clone https://github.com/asdf-vm/asdf.git ~/.asdf
cd ~/.asdf
git checkout "$(git describe --abbrev=0 --tags)"

echo -e '\n. $HOME/.asdf/asdf.sh' >> ~/.bash_profile
echo -e '\n. $HOME/.asdf/completions/asdf.bash' >> ~/.bash_profile

brew install \
  coreutils automake autoconf openssl \
  libyaml readline libxslt libtool unixodbc
```

# z

```shell
brew install wget
cd ~ && wget https://raw.githubusercontent.com/rupa/z/master/z.sh

```

# fzf

```shell
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install --key-bindings --completion --no-update-rc --no-bash --no-zsh
```

# asdf nodejs

```shell
brew install coreutils gpg
asdf plugin-add nodejs https://github.com/asdf-vm/asdf-nodejs.git
bash ~/.asdf/plugins/nodejs/bin/import-release-team-keyring

asdf install nodejs 10.15.3
asdf install nodejs 8.15.1
asdf global nodejs 10.15.3
```

# yarn

```shell
brew install yarn --ignore-dependencies
```

# shellcheck

```shell
brew install shellcheck

```

# ocaml

```shell
asdf plugin-add ocaml
asdf install ocaml 4.06.1
```

# python

issues:

- https://github.com/pyenv/pyenv/wiki/Common-build-problems
- https://developer.apple.com/documentation/xcode_release_notes/xcode_10_release_notes#3035624

```shell
brew install openssl readline sqlite3 xz zlib

export LDFLAGS="-L/usr/local/opt/openssl/lib"
export CPPFLAGS="-I/usr/local/opt/openssl/include"

export LDFLAGS="-L/usr/local/opt/readline/lib"
export CPPFLAGS="-I/usr/local/opt/readline/include"

export LDFLAGS="-L/usr/local/opt/sqlite/lib"
export CPPFLAGS="-I/usr/local/opt/sqlite/include"

export LDFLAGS="-L/usr/local/opt/zlib/lib"
export CPPFLAGS="-I/usr/local/opt/zlib/include"

asdf plugin-add python
asdf install python 2.7.15
asdf install python 3.7.1
asdf global python 3.7.1 2.7.15
```

# ruby

```shell
asdf plugin-add ruby https://github.com/asdf-vm/asdf-ruby.git
asdf install ruby 2.5.3
asdf global ruby 2.5.3
```

# fonts

```shell
brew tap caskroom/fonts
brew cask install font-hack-nerd-font
```
