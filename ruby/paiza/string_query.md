## N 個の文字列 S_1, ... , S_N と、Q 個の文字列 T_1, ... , T_Q が与えられる。 S_j == T_i を満たす最小の j を出力する。ただし、そのような j が存在しない場合は -1 を出力する。

```ruby
n, q = gets.split.map(&:to_i)

n_strings = n.times.map { gets.chomp }

q_strings = q.times.map { gets.chomp }

q_strings.each do |query|
  index = n_strings.index(query) # `query` が `n_strings` 内に存在するかチェック
  if index
    puts index + 1 # 見つかった場合、1-indexed で出力
  else
    puts -1 # 見つからない場合は -1 を出力
  end
end
```