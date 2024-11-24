## N 個の要素からなる数列 A が与えられる。2 ≦ i ≦ N の各 i に対して、A_i と同じ値が A_1 から A_{i-1} の間にあるかどうかを判定。

```ruby
# 入力を取得
n = gets.to_i
a = gets.split.map(&:to_i)

# 重複チェック用のセットを用意
seen = Set.new

# 各 i に対する判定
1.upto(n - 1) do |i|
  if seen.include?(a[i])
    puts "Yes"
  else
    puts "No"
  end
  # 現在の値をセットに追加
  seen.add(a[i - 1])
end
```