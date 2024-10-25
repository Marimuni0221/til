```ruby
n, a, b = gets.split.map(&:to_i)

# "(a, b)" という形式の文字列を N 個生成し、カンマと半角スペースで結合
result = Array.new(n, "(#{a}, #{b})").join(', ')

puts result
```

## 例
3 10 99
=>(10, 99), (10, 99), (10, 99)