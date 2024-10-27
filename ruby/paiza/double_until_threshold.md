# 整数  N  を2倍していき、 N  が  K  以上になるまでの操作回数  M  を求める
( N  を何回2倍すれば  K  に達するか、または超えるかを計算する問題)

```ruby
# 入力を受け取る
n, k = gets.split.map(&:to_i)

# 操作回数をカウントする変数
count = 0

# N が K 以上になるまで 2 倍し続ける
while n < k
  n *= 2
  count += 1
end

# 結果を出力
puts count
```