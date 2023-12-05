# yaml basics

description

### array

description

```ruby
require 'yaml'

yaml = DATA.read

puts YAML.load(yaml).inspect

__END__

- first
- second
- third
- fourth

```

### array of arrays

description

```ruby
require 'yaml'

yaml = DATA.read

puts YAML.load(yaml).inspect

__END__

-
  - first
  - second
-
  - third
  - fourth
-
  - fifth
  - sixth

```

### hashmap of string keys

description

```ruby
require 'yaml'

yaml = DATA.read

puts YAML.load(yaml).inspect

__END__

first: one
second: two
third: three
fourth: four

```

### hashmap of symbol keys

description

```ruby
require 'yaml'

yaml = DATA.read

puts YAML.load(yaml).inspect

__END__

:first: one
:second: two
:third: three
:fourth: four

```

### array of hashmaps

description

```ruby
require 'yaml'

yaml = DATA.read

puts YAML.load(yaml).inspect

__END__

- first: one
  second: two
- first: one
  second: two
- first: one
  second: two

```

### applying defaults with aliases

description

```ruby
require 'yaml'

yaml = DATA.read

puts YAML.load(yaml).inspect

__END__

default: &default
  first: one
  second: two
  third: three

data:
  - <<: *default
  - <<: *default

```
