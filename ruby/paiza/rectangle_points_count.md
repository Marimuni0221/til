## 長方形の内部や辺上に含まれる点の数を数える問題

```ruby
# 入力を受け取る
n = gets.to_i
points = n.times.map { gets.split.map(&:to_i) }
x_s, x_t = gets.split.map(&:to_i)
y_s, y_t = gets.split.map(&:to_i)

# 長方形の範囲を計算
x_min, x_max = [x_s, x_t].min, [x_s, x_t].max
y_min, y_max = [y_s, y_t].min, [y_s, y_t].max

# 長方形に含まれる点の数を数える
count = 0
points.each do |x, y|
  if x_min <= x && x <= x_max && y_min <= y && y <= y_max
    count += 1
  end
end

# 結果を出力
puts count
```