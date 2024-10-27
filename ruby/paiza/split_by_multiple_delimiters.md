```ruby
s = gets.chomp
puts s.split(/[\/:]/)
```

## 詳細
•	/[\/:]/ の部分で、[\/:] はスラッシュ（/）とコロン（:）のどちらかに一致するという意味。
•	\ は [ と ] の中で / を文字として扱うために使われている(エスケープするため)

• %r{} 記法ではエスケープを省略することも可能
```ruby
s = gets.chomp
puts s.split(%r{[/:]})
```