## xとyが正の整数で、次の条件を満たす組み合わせのうち、x * yが最大になるようなものを求める必要がある。

条件
	1.	 x + y < 100 
	2.	 x^3 + y^3 < 100000 

```ruby
max_product = 0

# xとyの全ての組み合わせを試す
(1...100).each do |x|
  (1...(100 - x)).each do |y|
    # 条件を満たすか確認
    if (x ** 3) + (y ** 3) < 100000
      # 条件を満たす場合、x * y の最大値を更新
      max_product = [max_product, x * y].max
    end
  end
end

puts max_product
```