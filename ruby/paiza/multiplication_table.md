# 与えられた配列Aのすべての要素について、掛け算の結果を行列形式で表示する。具体的には、配列Aの各要素同士を掛け算して、N x Nの掛け算表Bを作成する。
```ruby
# 入力の読み込み
n = gets.to_i
a = gets.split.map(&:to_i)

# 掛け算表の作成と出力
n.times do |i|
  row = []
  n.times do |j|
    row << a[i] * a[j]
  end
  puts row.join(" ")
end
```