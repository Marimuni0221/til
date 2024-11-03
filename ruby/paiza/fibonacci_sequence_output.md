## 指定された数 N 番目までのフィボナッチ数列を求め、改行区切りで出力する

```ruby
# 入力の読み込み
n = gets.to_i

# フィボナッチ数列を生成
fibonacci = [0, 1]
(2...n).each do |i|
  fibonacci << fibonacci[i - 2] + fibonacci[i - 1]
end

# フィボナッチ数列の出力
puts fibonacci[0...n]
```