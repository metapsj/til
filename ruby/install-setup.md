# install and setup ruby

requirements

- macos
- homebrew

steps

- homebrew
- chruby
- ruby-install
- zsh
- direnv

---

### installation

install chruby and ruby-install

```shell
$ brew install chruby ruby-install
```

verify ruby-install has been installed

```shell
$ ruby-install --version
```

verify chruby has been installed

```shell
$ chruby --version
```

configure chruby for zsh

```shell
# ~/.zshrc

# enable chruby
source /usr/local/share/chruby/chruby.sh
source /usr/local/share/chruby/auto.sh
chruby ruby-3.1.0

```

list available rubies

```shell
$ ruby-install --latest
```

install latest ruby

```shell
$ ruby-install --latest ruby
```

configure default ruby

```shell
$ chruby ruby-3.1.0
```

verify latest ruby is installed

```shell
$ ruby --version
```

configure .envrc plugins for direnv

```shell
# ./.envrc

ruby-version
dotenv
```

configure .ruby-version for direnv

```shell
# ./.ruby-version

ruby-3.1.0
```

source / activate direnv configuration

```shell
$ direnv allow
```

---
