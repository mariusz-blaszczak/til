I was investigating what commit of minitest caused my test to break and wanted to do git bisect, but minitest have no gemspec

Adding gemspec:
```ruby
# ./minitest/minitest.gemspec
Gem::Specification.new do |s|
  s.name         = "minitest"
  s.version      = "1000"
  s.platform     = Gem::Platform::RUBY
  s.required_rubygems_version = ">= 1.3.6"
  s.files        = Dir.glob("lib/**/*")
  s.require_path = "lib"
  s.summary      = "Make do with a self written gemspec"
  s.authors = 'Mariusz'
end
```

and using path in Gemfile:
```ruby
gem 'minitest', '1000', path: './minitest'
```

worked.
