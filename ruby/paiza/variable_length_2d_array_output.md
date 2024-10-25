```ruby
# 入力を取得
n, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)

# 開始位置を初期化
start_index = 0

# b の各値に従って a の部分配列を出力
b.each do |count|
  # 部分配列を切り出して出力
  puts a[start_index, count].join(' ')
  # 開始位置を更新
  start_index += count
end
```