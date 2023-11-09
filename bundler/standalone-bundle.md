# bundle --standalone

The `--standalone` option obviates the need for rubygems or bundler at runtime by
generating a `./gems/bundler/setup.rb` file.

```shell
bundle install --standalone --path=./gems
```

```ruby
# load_path.rb
bundler_standalone_loader = 'gems/bundler/setup'

begin
  require_relative bundler_standalone_loader
rescue LoadError
  warn "WARNING: Standalone bundle loader is not at #{bundler_standalone_loader}. Using Bundler to load gems."
  require "bundler/setup""
  Bundler.setup
end
```

```ruby
# config/application.rb
require_relative '../load_path'
require_relative 'boot'
```
