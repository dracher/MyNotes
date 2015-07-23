## 1. Where Ruby Finds Its Libraries

```
$ ruby -e 'puts $:'
```

## 2. Build Environment

```ruby
require 'rbconfig'
include RbConfig
CONFIG["host"]
# => "x86_64-apple-darwin12.2.0"
CONFIG["libdir"] # => "/Users/dave/.rvm/rubies/ruby-2.0.0-p0/lib"
```