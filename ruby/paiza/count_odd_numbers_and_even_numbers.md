# Rubyで数列の中の偶数と奇数の個数をカウントする方法
```ruby
# 数列の長さと要素を受け取る
n = gets.to_i                  # 数列の長さ
numbers = gets.split.map(&:to_i) # 数列の要素

# 偶数と奇数のカウント
even_count = numbers.count { |num| num.even? }
odd_count = numbers.count { |num| num.odd? }

# 結果を出力
puts "偶数の個数: #{even_count}"
puts "奇数の個数: #{odd_count}"
```