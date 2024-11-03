# Rubyで文字が大文字か小文字かを判定

## 1. 正規表現を使った方法
```ruby
char = 'A'

if char.match?(/[A-Z]/)
  puts '大文字です'
elsif char.match?(/[a-z]/)
  puts '小文字です'
else
  puts '大文字でも小文字でもありません'
end
```

## 2. upcase と downcase メソッドを使った方法
```ruby
char = 'a'

if char == char.upcase
  puts '大文字です'
elsif char == char.downcase
  puts '小文字です'
else
  puts '大文字でも小文字でもありません'
end
```

## 3. between? メソッドを使った方法
```ruby
char = 'B'

if ('A'..'Z').include?(char)
  puts '大文字です'
elsif ('a'..'z').include?(char)
  puts '小文字です'
else
  puts '大文字でも小文字でもありません'
end
```
