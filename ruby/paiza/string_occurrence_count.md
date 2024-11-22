## 辞書順に文字列の出現回数をカウントして出力する

```ruby
# 入力を取得
n = gets.to_i
strings = n.times.map { gets.chomp }

# 出現回数をカウント
counts = Hash.new(0)
strings.each do |s|
  counts[s] += 1
end

# 辞書順に並べ替えて出力
counts.sort.each do |key, value|
  puts "#{key} #{value}"
end
```