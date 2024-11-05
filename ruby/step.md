## Rubyの範囲を指定して、ある間隔ごとに値を取り出すメソッド

###	start.step(limit, step) の形式で使用します。
	•	start: 開始の値（この場合は i * i など）
	•	limit: 終了の値（ここでは n）
	•	step: 増加の間隔（ここでは i）

```ruby
2.step(10, 2) { |num| puts num }
```

### 出力結果
```ruby
2
4
6
8
10
```
