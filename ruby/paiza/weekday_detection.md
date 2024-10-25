# ある月の X 日が何曜日かを短縮表記で出力するプログラム。
  条件、1日は日曜日（Sun）、2日は月曜日（Mon）。

```ruby
# 曜日を短縮表記で格納した配列
days = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"]

# X日目を入力として取得
x = gets.to_i

# 曜日を計算（0-indexedにするために -1 する）
day_of_week = days[(x - 1) % 7]

# 結果を出力
puts day_of_week
```