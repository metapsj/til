# yaml basics

description

### array

description

```ruby
require 'yaml'

yaml = <<~EOS
  - first
  - second
  - third
  - fourth
EOS

puts YAML.load(yaml).inspect
```

### array of arrays

description

```ruby
require 'yaml'

yaml = <<~EOS
  -
    - first
    - second
  -
    - third
    - fourth
  -
    - fifth
    - sixth
EOS

puts YAML.load(yaml).inspect
```

### hash

description

```ruby
require 'yaml'

yaml = <<~EOS
  :first: one
  :second: two
  :third: three
  :fourth: four
EOS

puts YAML.load(yaml).inspect
```

### array of hashes

description

```ruby
require 'yaml'

yaml = <<~EOS
  - :first: one
    :second: two
  - :first: one
    :second: two
  - :first: one
    :second: two
EOS

puts YAML.load(yaml).inspect
```
