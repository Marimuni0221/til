文字列の置換
# 正規表現を使わない場合
"文字列".gsub("置換したい文字列", "置換後の文字列")
# 正規表現を使う場合
"文字列".gsub(/正規表現/, "正規表現に該当した箇所を置換した後の文字列")

#例
"abcdefg".gsub("def", "aa")
#=> "abcaag"

"abcdefg".gsub(/def/, "aa")
#=> "abcaag"

"abcabc".gsub(/b/, "<<\&>>")
#=> "a<<b>>ca<<b>>c"