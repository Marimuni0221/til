## 与えられた整数Nに対して、2以上N以下の素数の個数を求める。素数は、約数が1とその数自身のみである自然数のこと。

```ruby
# 入力の読み込み
n = gets.to_i

# 素数判定のための配列を作成（初期値はtrue）
is_prime = Array.new(n + 1, true)
is_prime[0] = is_prime[1] = false  # 0と1は素数ではないので除外

# エラトステネスの篩(ふるい)で素数をマーク
(2..Math.sqrt(n)).each do |i|
  if is_prime[i]
    (i * i).step(n, i) do |j|
      is_prime[j] = false
    end
  end
end

# 素数の数をカウント
prime_count = is_prime.count(true)
puts prime_count
```

### 1.	素数判定用の配列作成：
•	配列is_primeを作成し、要素数はn + 1にする。この配列で、インデックス番号が素数かどうかをtrueまたはfalseで示。
•	初期状態では、すべての要素をtrueに設定するが、0と1は素数ではないため、falseに設定。

### 2.	エラトステネスの篩の適用：
•	2からMath.sqrt(n)までの数をループで確認。これにより、nまでのすべての数の倍数を除外して素数を見つけられう。
•	もしiが素数であれば、その倍数（i*iから始まりiずつ増加する数）をfalseに設定。

### 3.	素数のカウント：
•	is_prime.count(true)で、配列の中のtrueの数、つまり素数の数をカウント。
