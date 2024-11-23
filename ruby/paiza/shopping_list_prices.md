## N 個の商品が売られており、i 番目の商品の名前は A_i で、価格は B_i。あなたは M 個の商品名が書かれたお買い物リスト S を持っている。リストに書かれているそれぞれの商品について、商店での価格を出力する。リストには 商店が扱っていない商品も書かれている可能性があるが、その場合は価格の代わりに -1 を出力する。

```ruby
# 標準入力を読み取る
n, m = gets.split.map(&:to_i)

# 商品情報をハッシュに格納
prices = {}
n.times do
  item, price = gets.split
  prices[item] = price.to_i
end

# お買い物リストの商品名を読み取り価格を出力
m.times do
  product = gets.chomp
  # ハッシュにキーが存在すれば価格、存在しなければ -1 を出力
  puts prices.fetch(product, -1)
end
```