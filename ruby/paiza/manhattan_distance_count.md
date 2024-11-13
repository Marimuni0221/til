## 与えられた点（n 番目の点）とのマンハッタン距離が k 以下の点の数を数える

```ruby
# 入力の取得
n = gets.to_i
points = []

# 点の座標を配列に格納
(n - 1).times do
  x, y = gets.split.map(&:to_i)
  points << [x, y]
end

# 最後の点の座標
x_n, y_n = gets.split.map(&:to_i)

# マンハッタン距離の閾値
k = gets.to_i

# マンハッタン距離が k 以下の点の数をカウント
count = 0
points.each do |x, y|
  distance = (x - x_n).abs + (y - y_n).abs
  count += 1 if distance <= k
end

# 結果の出力
puts count
```
