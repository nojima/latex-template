latex-template
==============

LaTeX を OMake を使って自動ビルドするためのテンプレートです．

次のようなディレクトリ構成を仮定しています．

    root
    ├ OMakeroot
    ├ OMakefile       このファイル
    ├ document.tex    TeXファイル (文字コードはUTF-8)
    ├ refs.bib        bibファイル (文字コードはUTF-8)
    ├ hogehoge/       サブディレクトリ (名前は任意)
    │ ├ sub1.tex      サブディレクトリにあるTeXファイルもコンパイルされる
    │ ├ sub2.tex      上に同じ
    └ images/         画像はimagesディレクトリの下に置く
       ├ fig01.png    png対応
       ├ fig02.jpg    jpg対応 (拡張子は必ずjpgにすること)
       └ fig03.eps    eps対応


## 使い方

1. `OMakefile` を環境にあわせて編集します．
2. `omake -P --verbose` を実行します．
3. OMake が走っている状況で，TeX ファイルを編集すると，自動的に PDF が更新されていきます．


## 注意

* TeX ファイルの文字コードは UTF-8 を仮定しています．
* デフォルトの設定は Windows 用になっています．
  * Windows 以外の環境の場合，`pbibtex` ではなく `jbibtex` を使う必要があったり，`--kanji=utf-8` が使えなかったりする可能性があります．

