## sliceメソッドは、Rubyの配列や文字列から指定した部分を取得するためのメソッド

### 1.インデックスを指定して取得
```ruby
array = [10, 20, 30, 40, 50]
puts array.slice(2)  # 出力: 30
```

### 2. 開始インデックスと長さを指定して取得
```ruby
array = [10, 20, 30, 40, 50]
puts array.slice(1, 3).inspect  # 出力: [20, 30, 40]
```

### 3.範囲オブジェクトで指定して取得
```ruby
array = [10, 20, 30, 40, 50]
puts array.slice(1..3).inspect  # 出力: [20, 30, 40]
puts array.slice(1...3).inspect # 出力: [20, 30]
```

### sliceメソッドと[]の違い
Rubyでは、[]を使って配列や文字列から部分を取得するのが一般的ですが、sliceメソッドも同じことが可能。実際にはarray[1..3]やstr[0, 5]などでsliceと同じ処理を行っている。
```ruby
array = [10, 20, 30, 40, 50]
puts array[1, 3].inspect  # 出力: [20, 30, 40]
```