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

install with homebrew

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

configure zsh

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

verify latest ruby is installed

```shell
$ ruby --version
```

configure direnv

```shell
$ direnv allow
```

---
