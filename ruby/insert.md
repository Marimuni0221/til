# Rubyで配列に要素を追加する際に、特定の位置に新しい要素を挿入するためのメソッド。このメソッドを使うと、配列内の指定したインデックスに新しい要素を挿入し、他の要素をその後ろにシフトすることができる。

## 基本構文
```ruby
array.insert(index, value)
```
	•	index: 挿入位置のインデックス（0から始まる）
	•	value: 挿入する要素

## 使用例
```ruby
array = [1, 2, 3, 4]
array.insert(2, 10)  # インデックス2の位置に10を挿入
puts array.inspect
```

```ruby
array = [1, 2, 3, 4]
array.insert(2, 10, 20, 30)  # インデックス2の位置に10, 20, 30を挿入
puts array.inspect
# 出力: [1, 2, 10, 20, 30, 3, 4]
```

## インデックスが配列の範囲外の場合
```ruby
array = [1, 2, 3]
array.insert(10, 99)  # インデックス10（範囲外）の位置に99を挿入
puts array.inspect
# 出力: [1, 2, 3, 99]
```