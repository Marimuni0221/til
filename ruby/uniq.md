# Rubyで配列内の重複した要素を削除するためのメソッド。このメソッドを使用すると、配列内のユニークな要素のみが残り、新しい配列が返される。

## 基本構文
```ruby
unique_array = array.uniq
```

## 使用例
```ruby
array = [1, 2, 3, 2, 4, 3, 5]
unique_array = array.uniq
puts unique_array.inspect
# 出力: [1, 2, 3, 4, 5]
```

## 元の配列を直接変更する場合（uniq!）
```ruby
array = [1, 2, 3, 2, 4, 3, 5]
array.uniq!
puts array.inspect
# 出力: [1, 2, 3, 4, 5]
```
