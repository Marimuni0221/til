## 入力として与えられた文字列内の各アルファベット（a～z）の出現回数を数える

```ruby
n = gets.to_i
s = gets.chomp

# 'a'から'z'までの各文字の出現回数を数える
char_count = ('a'..'z').map { |char| s.count(char) }

# 結果を出力
puts char_count.join(" ")
```