## 文字列 S を先頭から順に見て、各数字が最初に現れた位置だけを残し、重複する数字を削除した結果を出力する

```ruby
s = gets.chomp
unique_digits = []

s.each_char do |char|
  unique_digits << char unless unique_digits.include?(char)
end

puts unique_digits.join
```