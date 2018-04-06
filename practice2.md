第二章
============
### 10. 行数のカウント
~~~~ 
wc -l hightemp.txt
~~~~

### 11. タブをスペースに置換
~~~~
expand -t 1 hightemp.txt
~~~~

### 12. 1列目をcol1.txtに，2列目をcol2.txtに保存
~~~~
cut -f 1 hightemp.txt > col1.txt #1列目について
cut -f 2 hightemp.txt > col2.txt #2列目について
~~~~

### 13. col1.txtとcol2.txtをマージ
~~~~
paste col1.txt col2.txt > col.txt
~~~~

### 14. 先頭からN行を出力
~~~~
head -n N hightemp.txt
~~~~

### 15. 末尾のN行を出力
~~~~
tail -n N hightemp.txt
~~~~

### 16. ファイルをN分割する
~~~~
split -l 2 hightemp.txt
~~~~

### 17. １列目の文字列の異なり
~~~~
cat hightemp.txt | awk '{print $1}' | sort | uniq
~~~~

### 18. 各行を3コラム目の数値の降順にソート
~~~~
cut -f 3 hightemp.txt | sort -r
~~~~

### 19. 各行の1コラム目の文字列の出現頻度を求め，出現頻度の高い順に並べる
~~~~
cut -f1 hightemp.txt | sort | uniq -c | sort --reverse
~~~~
