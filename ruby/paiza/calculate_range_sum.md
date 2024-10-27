# 数列 numbers の a 番目から b 番目までの要素を配列のスライスで取得し、その合計を計算する

```ruby
n, a, b = gets.split(' ').map(&:to_i)
numbers = gets.split(' ').map(&:to_i)

# 配列の a 番目から b 番目までの要素を取得して合計を計算
sum = numbers[(a - 1)..(b - 1)].sum

puts sum
```