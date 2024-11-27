## N 個の要素からなる数列 A が与えられる。2 ≦ i ≦ N の各 i に対して、A_i と同じ値が A_1 から A_{i-1} の間にあるかどうかを判定する。

```ruby
require 'set' 
n = gets.to_i
a = gets.split.map(&:to_i)

# 確認済みの値を保持する集合
seen = Set.new

(1...n).each do |i|
  if seen.include?(a[i])
    puts 'Yes'
  else
    puts 'No'
  end
  # 現在の値を集合に追加
  seen.add(a[i - 1])
end
```