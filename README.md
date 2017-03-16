# Introduction to Data Science with Julia

データサイエンスの講義用に作成している講義ノートの草案です。

[JuliaBox](https://juliabox.com/)で使うことを想定しています。
ローカルで使用する場合は適宜パッケージを追加してください。

## ファイル概要
- notebook: 講義ノート
  - 連番ファイルが講義で使用する資料
  - Plots.jl_example.ipynb は Plots.jl を使っての描写の例
  - titanic: 最終課題のアプローチの仕方のサンプル
  - soln.zip: 練習問題の解答例. zip を解凍するにはパスワードが必要.
- tex: notebook を TeX にしたもの
- data: 講義で使用するサンプルデータ
- lectures.md: データサイエンスを勉強するときに参考になる講義などのリスト
- jsarticle.tplx: notebook を TeX に変換するときに用いるテンプレート


## JuliaBox 使用上の注意
JuliaBox ではファイル名に日本語を入れることは出来ません。(日本語が入っているとファイルが表示されません。)  
そのため新しく notebook を作る場合はファイル名は半角英数字にしてください。

パッケージが上手く読み込めない場合は一度 Console で Julia を立ち上げ、
```julia
Pkg.update()
```
でパッケージをアップデートすると上手くいくかもしれません。

## 講義で使用する方へ
学生に同期させたブランチのファイル(notebookなど)を編集すると、再度学生が同期した際に競合が起こる可能性があるため注意してください。  
訂正や加筆をする場合ブランチを切り替えてください。

## notebook を TeX に変換
```bash
$ jupyter-nbconvert --to latex foo.ipynb --template jsarticle.tplx
$ uplatex foo
$ dvipdfmx foo
```

参考
[jupyter notebookをLaTeXに変換 - Qiita](http://qiita.com/tttamaki/items/58ab3250202d2c17e233)


## License
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br /><span xmlns:cc="http://creativecommons.org/ns#" property="cc:attributionName">goropikari</span> 作『<span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Introduction to Data Science with Julia</span>』は<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">クリエイティブ・コモンズ 表示 - 非営利 - 継承 4.0 国際 ライセンス</a>で提供されています。
