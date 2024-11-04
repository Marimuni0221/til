## 行列の転置を求める。転置行列は、もとの行列の行と列を入れ替えたもの。例えば、もとの行列AがN行K列のとき、転置行列はK行N列となる。

```ruby
# 入力の読み込み
n, k = gets.split.map(&:to_i)
matrix = []
n.times do
  matrix << gets.split.map(&:to_i)
end

# 転置行列の作成
transpose = Array.new(k) { Array.new(n) }
(0...n).each do |i|
  (0...k).each do |j|
    transpose[j][i] = matrix[i][j]
  end
end

# 転置行列の出力
transpose.each do |row|
  puts row.join(" ")
end
```