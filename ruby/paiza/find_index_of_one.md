# 数列の中から値 1 がある位置（何番目か）を見つけて出力する
```ruby
n = gets.to_i
a = gets.split.map(&:to_i)

# 配列 a の中で 1 の位置を検索し、1 を加えて出力
puts a.index(1) + 1
```