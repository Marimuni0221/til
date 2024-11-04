## 二次元配列の中で1の値がある場所（行と列のインデックス）を探し、その位置を出力する
```ruby
# 入力の読み込み
n, k = gets.split.map(&:to_i)
matrix = []
n.times do
  matrix << gets.split.map(&:to_i)
end

# 二次元配列の中で1の位置を探す
(0...n).each do |i|
  (0...k).each do |j|
    if matrix[i][j] == 1
      # 見つけたら、行と列を出力して終了
      puts "#{i + 1} #{j + 1}"
      break
    end
  end
end
```