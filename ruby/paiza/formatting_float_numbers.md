```ruby
n = gets.to_f

# 小数第3位まで表示し、それ以降を四捨五入する
formatted_number = format("%.3f", n)
puts formatted_number
```

# format("%.3f", n)
•	format メソッドを使って、数値を「小数点以下3桁」までの文字列に変換。

## 	"%.3f" の解釈
•	% はフォーマット指定子の開始。
•	.3 は小数点以下の桁数を指定。
•	f は浮動小数点数（小数）の形式で出力することを意味する。
