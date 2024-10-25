Rubyで文字列として書かれたRubyコードを実行するためのメソッド
# 基本的な使い方
result = eval("1 + 2")
puts result  # => 3

# 変数や式の評価
x = 10
y = 5
result = eval("x * y")
puts result  # => 50

# メソッドの呼び出し
def greet
  "Hello, world!"
end

puts eval("greet")  # => "Hello, world!"

*但し、セキュリティリスクがある為、他のメソッドを使う方が良い