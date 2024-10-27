```ruby
n = gets.to_i
factorial = 1
(1..n).each do |num|
    factorial *= num
end

count = 0
while factorial % 10 == 0
    count += 1
    factorial /= 10
end
puts count
```