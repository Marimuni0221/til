## 配列AとBの各要素の積の中で最大の値を求める
```ruby
# 入力の読み込み
n, k = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)

# 積の最大値を求める
max_product = -Float::INFINITY
a.each do |ai|
  b.each do |bi|
    product = ai * bi
    max_product = [max_product, product].max
  end
end

# 結果の出力
puts max_product
```