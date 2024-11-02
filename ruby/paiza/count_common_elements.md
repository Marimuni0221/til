## a と b の両方に存在する共通の要素をカウントする

```ruby
n = gets.to_i
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)

# 共通の要素を取得し、その数を出力
common_elements = a & b
puts common_elements.length
```