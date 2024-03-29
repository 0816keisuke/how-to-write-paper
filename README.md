# 論文執筆アンチパターンチェック表

本ページでは論文を執筆する際に意識すること・注意すること等を記載しています．  
また [see_also](https://github.com/0816keisuke/how-to-write-paper/tree/main/see_also) では，本記事以外にも参照すべきサイト等を掲載していますので，そちらも参照した上で論文執筆をしてください．  
皆さんの論文執筆がより良いものになりますように！

※ 「こういった注意事項などもあるよ」といったアドバイスや，追加での補足事項，誤植などがありましたら，[Issue #1](https://github.com/0816keisuke/how-to-write-paper/issues/1) へコメントください．

## 論文執筆のフロー

1. 論文を執筆する．
2. 何度も何度も何度も推敲する，死ぬほど推敲する．
3. 何度も何度も何度も見直す，死ぬほど見直す．
4. 最終チェックして，誰かに出して添削してもらう．

⚠️ 見直し・推敲の際は，ソースコードではなくPDFを見るようにしましょう．
ソースコードが(一見)ちゃんと書けているように見えても，あなたの想像通りにPDFが出力されているとは限らないです．
実は図が歪んでいたり，はみ出していたりなど，十分に有り得ます．

⚠️ 1回見直したくらいでは，完璧になりません．
大抵の人は見落としがあります．
人に添削してもらう時は(極論)100回くらい見直してから出しましょう．
些細なミスを指摘するのはお互いの時間を無駄にするだけです．
もちろん安易なミスを常に無くして完璧にする，ということは難しいので，「やってしまった！」がたまーにあるのは仕方のないことですが，そういったことが極力なくせるようにまずは心がけていきましょう．

究極的に言いたいことは，**「最大限の思いやりを持って書く」** ということです．

- 相手に見てもらう以上，安易なミスはしない．
- 読者の頭にすんなり入ってくるような，一発で理解できるような文章を書く．

⚠️⚠️⚠️ **「相手に時間をとって読んでもらう」ということを常に意識するように** ⚠️⚠️⚠️

## Texについて

- Texでコンパイルエラーに遭遇した時は，まずは自力で解決しようと粘りましょう．エラー時にはエラーメッセージが必ず出ているので，まずはググって自分で解決する力を身につけてください．ほぼ全てのエラーの解決策がネットに落ちています．その際，日本語記事を探してもいいですが，英語記事の方がよっぽど情報が豊富なので，英語記事を参考にすることをおすすめします(日本語のスタイルファイル特有のエラーなどは除く)．
- 十二分に尽力したけどそれでもエラーが解決できない時は，誰かに助けを求めましょう．
    - その際，単に「このエラーが解決できないです」とは言わないように．目的(どういうことがしたいか)，現状(どこまで自分で調べて分かっているのか)などもしっかり添えて共有しましょう．言葉で伝えない限り，あなたの頭の中を他人は理解してくれません．
    - Texのコンパイルエラーだけでなく，プログラムのエラー共有などにも共通です．**「相手にとって再現性がしっかり保てる」** ような共有をしましょう．

## 日本語論文のチェック表

### ケアレスミス

- 誤字・脱字はないか？  
  100回見直しましょう．これに尽きます．
- 句読点(「、」「。」)を使ってないか？  
  全文検索して確認しよう．
- 文中の「，」「．」は全て全角になっているか？  
  全文検索して確認しよう．
- 表記揺れがないか？  
  全文検索して確認しよう．
  - 「イジングマシン」と「実イジングマシン」
  - 「ソルバ」と「ソルバー」  
- アラビア数字と漢数字が混ざってないか？
  - 「1つ」と「一つ」
- 文中で使用している変数は数式モードになっているか？
- 二重動詞になってないか？
  - ❌：実験を行う，⭕️：実験する
  - ❌：求解することができる，⭕️：求解できる
- 式番号や章番号の引用で使う`\ref{}`コマンドは全て正しく機能しているか？「??」になっていないか？
  - ❌：図??では，⭕️：図3では
- (必要であれば)謝辞を書いているか？

### 文章表現

- 同じ内容の文章を重複して書いていないか？
- 冗長な表現になっていないか？もっとシンプルに言い換えられないか？
- 使用した変数は文章中で全て定義/説明されているか？
- 結果は定量的に述べられているか？

### 図・表

- 図表タイトルの末尾にはピリオドが打たれているか？
- 図中の文字のフォントは適切な大きさか？小さすぎないか？大きすぎないか？
- 文中で使用していない・定義していない言葉や変数を図表中に用いていないか？
  - 逆も然り．図表中で使用している言葉や変数を文中で説明しているか？

### 参考文献

- 参考文献のフォーマットは正しいか？
- 参考文献中の論文タイトルにおいて，大文字になるべきところが小文字になっていないか？
    - ❌：english，⭕️：English
    - ❌：ising，⭕️：Ising
- 雑誌名は正しいか？(大文字小文字など)
    - ❌：nature physics，⭕️：Nature Physics
    - ❌：siam，⭕️：SIAM
- サイトを引用する時，引用された形式が変になっていないか？  
  特に，ウェブサイトを引用するとURLの形が崩れることが多いです．変なところで改行されたり，逆に全く改行されずに用紙を突き抜けたりすることがあります．

### その他のポイント

- 「説明する」や「述べる」といった言葉はできるだけ避ける．
- 「について」は「を」で言い換えできれば「を」とする．
- 1つ前の文章と結びを同じにするのはなるべく避ける．
- 「そこで本稿では」というような文章の前では必ず改行する．
- なるべく自分の研究機関(自身が所属する研究室など)以外のものも引用する(例えば，手法比較など)  
  自分の研究機関しか引用していないと，他の研究機関のことを追っていないのかと思われる．
- 章構成を記述するときには，改行をしない．
- 章タイトルなどは途中で改行しない．改行はTeXに任せる．
- 「悪い」という言葉はあまり使わない(大きいとか，小さいとか，〜〜と比較して，という言葉に置き換える)．

## 英語論文のチェック表

本章でも，[上記の日本語論文のチェック表](https://github.com/0816keisuke/how-to-write-paper#%E6%97%A5%E6%9C%AC%E8%AA%9E%E8%AB%96%E6%96%87%E3%81%AE%E3%83%81%E3%82%A7%E3%83%83%E3%82%AF%E8%A1%A8)で記載したことが共通で言えることが多々あるので，まずはそちらを参照すべし．

また，英語論文の執筆時には[Hyper Collocation](https://hypcol.marutank.net/ja/)を有効活用することで，自分の使おうとしてる語彙が自然かどうかもチェックしよう．

### ケアレスミス

[まずはこちらを参照されたり](https://github.com/0816keisuke/how-to-write-paper#%E3%82%B1%E3%82%A2%E3%83%AC%E3%82%B9%E3%83%9F%E3%82%B9)

- 文法は正しいか？(三単現のs，複数形，冠詞a/anなど)
- 文中のカンマ，ピリオドは全て半角になっているか？
- 半角カンマ，ピリオドの後に半角スペースが挿入されているか？
- 文章の途中で数式を挿入している場合，数式の最後にピリオドが打たれているか？
- 省略形は使われていないか？  
  論文は正式な文章なので，省略した形を使いません．
  - ❌ : doesn't, ⭕️ : does not
- 脚注番号はカンマの後に来ているか？
- 1,000以上の数字には適切な位置にカンマが打たれているか？
  - ❌ : 1234, ⭕️ : 1,234
- タイトルなどにおいて，前置詞は小文字になっているか？
- 人称は問題ないか？
  - youは原則使わない

### 図・表

[まずはこちらを参照されたり](https://github.com/0816keisuke/how-to-write-paper#%E5%9B%B3%E8%A1%A8)

- 図はすべて英語になっているか？
- 単位の前に半角スペースが挿入されているか？(ただし，%と℃は例外)
  - ❌ : execution time[s], ⭕️ : execution time [s]
  - ❌ : 10V, ⭕️ : 10 V

### 参考文献

[まずはこちらを参照されたり](https://github.com/0816keisuke/how-to-write-paper#%E5%8F%82%E8%80%83%E6%96%87%E7%8C%AE)

### その他のポイント
