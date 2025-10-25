# 4.参考文献｜Reference
文責：堀江和正

[English Version](README_en.md)

---

アイザック・ニュートンはかつてこう言いました。

> “If I have seen further, it is by standing on the shoulders of giants.”
> 「私がより遠くを見渡せたのだとすれば、それは巨人たちの肩の上に立っていたからだ。」

この言葉は、科学や学問における進歩の本質を見事に表しています。  
私たちの研究は、完全な「独創」ではなく、過去の知識の積み重ねの上に成り立つものです。  
そのため、先人の知見を適切に引用し、学問の系譜の中に自らの研究を位置づけることが不可欠です。  

## 参考文献とは何か

**参考文献:References**とは、自分の研究・論文を支える他者の成果を明示するための情報リストです。  
論文における参考文献は、単なる「引用元の一覧」ではなく、次のような意味を持ちます。  

自分の主張の根拠を明確にする  
→ 「この考え方は過去にどのような議論に基づいているのか」を読者に示す。  

先行研究を尊重し、知的誠実性を担保する  
→ 他人の成果を自分のものと誤解させないための倫理的基盤。  

学問的対話の中に位置づける  
→ 「自分の研究がどの文脈の上に、何を更新したのか」を明確化する。  

## なぜ参考文献が重要なのか

参考文献を示すことは、研究の信用と再現性を担保するための第一歩です。  
研究は、事実やデータだけでなく、他者による理論・方法・議論に支えられています。

適切に文献を明示することで、  
「この研究はどの問題系を継承し、どの課題を更新しているのか」を明快に示すことができます。

## 参考文献の例

> Stephansen, J.B., Olesen, A.N., Olsen, M. et al. Neural network analysis of sleep stages enables efficient diagnosis of narcolepsy. Nat Commun 9, 5229 (2018).

著者，論文のタイトル，掲載誌，掲載誌の番号（〇号），記事番号 OR ページ，掲載年  
といった，論文を特定するために必要な情報がすべて含まれています．

また，論文を特定する方法としてDOIを記載する場合もあります．  
これは，全ての論文に振られた固有のIDのことで，特定を容易にするためにつけられています．  

例えば，上の参考文献には，
`10.1038/s41467-018-07229-3`
というDOIが振られており，このDOIでWeb検索をすると一発で出てきます．

参考文献として，どの情報を入れるか，どのように表記するか（順番や氏名表記方法），といったルールは，
原則として**論文誌ごとに異なります．**  

Wordで論文を執筆する場合，論文誌ごとに表記を変更する必要がありますが，  
以下で紹介しているLaTeXのシステムを使うと，学会が配布しているテンプレートを利用するだけで表記を合わせることができます．

---

## LaTeXにおける参考文献の利用方法

LaTeXでは，bibtexと呼ばれるシステムを用いることで，容易に参考文献の提示をすることができます．  
手順は以下の通りです．

1. 参考文献 `.bib` を用意する（入手／作成）
2. LaTeX 原稿から `.bib` を読み込む
3. LaTeXコンパイル時にbibtexも利用する．

1から順番に見ていきましょう．

## `.bib`ファイルと入手/作成方法

まず，`.bib`ファイルは書誌情報が書かれたテキストの拡張子を変更し`.bib`にしたファイルです．  
具体的には以下が記述されています．

```bib
@article{Stephansen2018,
  author = {Stephansen, Jesper B. and others},
  title = {Neural network analysis of sleep stages enables efficient diagnosis of narcolepsy},
  journal = {Nature Communications},
  year = {2018},
  volume = {9},
  number = {5229},
  doi = {10.1038/s41467-018-07229-3}
}
```

各行の意味は，

- `@article{Stephansen2018,`:  
参考文献が論文＝articleであることを示すとともに，この文献に名前（Stephansen2018）を付けています．  
- `author = {Stephansen, Jesper B. and others},`:  
著者  
- `title = {Neural network analysis of sleep stages enables efficient diagnosis of narcolepsy},`:
論文のタイトル  
- `journal = {Nature Communications},`
論文誌  
- `year = {2018},`:
掲載年  
- `volume = {9},`:
雑誌の号数  
- `number = {5229},`:
記事の番号  
- `doi = {10.1038/s41467-018-07229-3}`:
DOI

です．

この他，ページ数を示すための`pages`なども存在しています．

論文の掲載ページには，これらの情報が記載されているので，これらをコピー＆ペーストすることで.bibファイルを作成することができます．

<img width="1643" height="831" alt="image" src="https://github.com/user-attachments/assets/91bd3bfd-a924-48b9-bcff-0a012cee04cf" />

**Nature Communicationの論文の例**

また，一部の論文誌では，直接.bibをダウンロードすることもできます．

<img width="1363" height="506" alt="image" src="https://github.com/user-attachments/assets/14c5c4fd-ddf0-40ea-aea3-1f4474a365a4" />

**Elsevier社の論文（Science Direct）の例**

これらの書誌情報を統合して，1つの`.bib`ファイルを作成してください．  
[参考](example.bib)



## ここまで理解したら，

ここまでで作成した`main.tex`に，図と表を加え，お手本の`main.pdf`に近づけましょう．  
図のファイルは本ディレクトリで配布しています．  
また，文中の??となっている部分は，元々図・表・数式の参照番号が入っていた部分です．  
`\label{}`,`ref{}`を用いて，適切な参照番号を割り振ってください．
