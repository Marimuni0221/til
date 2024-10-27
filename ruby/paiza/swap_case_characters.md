# 文字を大文字・小文字に変換

```ruby
s = gets.chomp.split('')

s.map! do |char|
  if char == char.upcase
    char.downcase
  else
    char.upcase
  end
end

puts s.join
```