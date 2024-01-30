WIP
based on /Users/mariusz/.rbenv/versions/3.0.2/lib/ruby/gems/3.0.0/gems/rspec-core-3.12.1/lib/rspec/core/bisect/example_minimizer.rb
There are following variables:
all_example_ids - whole suite tests
failed_example_ids - ???
remaining_ids - ??

1. It first run all rspec suite to find:
   1. all_example_ids
   2. failed_example_ids - ids of failed examples
   3. ramaining_ids = all_example_ids - failed_example_ids
2. Then it takes ramaining_ids, split it by 2 and for each halve run rspec: remaining_ids - ids + failed_example_ids  
3. If rspec fails with the same error for a halve, then all ids of a halve are removed from remaining_ids
4. If rspec does not fail for a halvek


