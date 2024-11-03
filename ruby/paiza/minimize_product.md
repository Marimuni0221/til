## 「A 以上 B 以下の範囲で任意に選んだ 2 つの整数  X  と  Y  の積  X * Y  の最小値」を求める

```ruby
a, b = gets.split(' ').map(&:to_i)

# 範囲に 0 が含まれる場合、最小の積は 0
if a <= 0 && b >= 0
  puts 0
# 範囲がすべて正の場合、最小の積は a * a
elsif b <= 0
    # AとBがともに負の場合、B*Bが最小
    puts b * b
elsif a >= 0
    # AとBがともに正の場合、A*Aが最小
    puts a * a
else
    puts [a * b, a * a, b * b].min
end
```