## 金額 Z を支払う際に、1円硬貨、X円硬貨、Y円硬貨の3種類を使い、硬貨の枚数が最小になるように支払う方法を求める。

### 解法のポイント

1.	組み合わせを試す：
•	Z円を支払うために、X円硬貨とY円硬貨を使う枚数の組み合わせを全て試し、その組み合わせに対して必要な1円硬貨の枚数を計算します。
2.	硬貨の最小枚数を見つける：
•	それぞれの組み合わせで必要な硬貨の合計枚数を計算し、その最小値を求めます。

### アルゴリズム

	1.	X円硬貨を使う枚数（x_count）を0から Z / X まで試します。
	2.	その中で、Y円硬貨の枚数（y_count）も0から Z / Y まで試します。
	3.	x_count * X + y_count * Yの合計が Z以下の場合、残りの金額は1円硬貨で支払います。
	4.	このときの合計硬貨数（x_count + y_count + 1円硬貨の枚数）を記録し、最小値を出力します。

```ruby
# 入力を取得
x, y, z = gets.split.map(&:to_i)

# 最小枚数を大きな初期値に設定
min_coins = Float::INFINITY

# X円硬貨とY円硬貨の組み合わせを全て試す
(0..(z / x)).each do |x_count|
  (0..(z / y)).each do |y_count|
    # 現在の組み合わせでの合計金額
    total = x_count * x + y_count * y
    
    # 合計が支払う金額zを超える場合はスキップ
    next if total > z

    # 残り金額を1円硬貨で支払う
    remaining = z - total
    total_coins = x_count + y_count + remaining
    
    # 硬貨の最小枚数を更新
    min_coins = [min_coins, total_coins].min
  end
end

# 結果を出力
puts min_coins
```  
