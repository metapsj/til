# homebrew sqlite

macos sqlite path

```shell
which sqlite3
```

homebrew sqlite path

```shell
echo $(brew --prefix sqlite)
```

gem install with homebrew sqlite

```shell
gem install sqlite3 -- --with-sqlite3-dir=$(brew --prefix sqlite)
```

or

gem install with homebrew sqlite

```shell
gem install sqlite3 -- --with-sqlite3-dir=$(brew --prefix sqlite)/bin/sqlite3
```

bundle config build with homebrew sqlite

```shell
bundle config build.sqlite3 --with-sqlite3-lib=$(brew --predix sqlite)/lib
```

bin stub with homebrew sqlite

```shell
# ./bin/sqlite3

#!/usr/bin/env sh

$(brew --prefix sqlite)/bin/sqlite3 $1
```
