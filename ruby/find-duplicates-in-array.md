nuniq = [1, 1, 2, 3]

duplicates = nuniq.tally.select { |_, count| count > 1 }.keys

puts duplicates.inspect  # Output: [1]
