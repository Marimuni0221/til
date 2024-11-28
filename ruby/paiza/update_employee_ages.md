## 社員の名前と昨年度の年齢が与えられたリストを基に、今年度の社員一覧表を作成する。今年度の年齢は昨年度の年齢に1を加えた値。リストを更新し、名前と今年度の年齢を出力する。

```ruby
# 入力を受け取る
n = gets.to_i
employees = []

# 社員情報を取得
n.times do
  s, a = gets.split
  employees << [s, a.to_i]
end

# 結果を出力
employees.each do |s, a|
  puts "#{s} #{a + 1}"
end
```