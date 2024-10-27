## 指定された位置に特定の文字を配置し、それ以外の位置を指定された文字で埋めることでパスワードを作成

```ruby
# 入力を取得
n = gets.to_i
q = gets.to_i

# パスワードを初期化
password = Array.new(n)

# 指定された位置に文字をセット
q.times do
  position, char = gets.split
  position = position.to_i - 1  # インデックスを0基準に調整
  password[position] = char
end

# C の入力を受け取り、未設定の部分を C で埋める
c = gets.chomp
password.map! { |char| char || c }

# パスワードを文字列として出力
puts password.join
```

・入力例
8
7
1 p
2 a
3 s
4 s
6 o
7 r
8 d
w