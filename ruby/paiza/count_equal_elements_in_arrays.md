# 整数 N と2つの数列 A と B が与えられ、それぞれの数列の対応する要素 A[i] と B[i] が等しいものの個数をカウントして出力する

```ruby
# 標準入力から値を取得
n = gets.to_i
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)

# A[i] と B[i] が等しいものの個数をカウント
count = 0
n.times do |i|
  count += 1 if a[i] == b[i]
end

# 結果を出力
puts count
```