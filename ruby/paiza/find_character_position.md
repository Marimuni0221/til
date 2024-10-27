# 文字列 S 内で指定された文字 c が現れる位置を調べて、その位置を1から始まる数で出力する

```ruby
s = gets.chomp
c = gets.chomp

# 文字 c の位置を 1 から始まる数で出力
puts s.index(c) + 1
```