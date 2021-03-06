vim の管理

`<Leader>`

マップコマンドで特別な文字列 "\<Leader>" を使用すると、その部分が変数
"mapleader" に設定された文字列で置き換わります。"mapleader" が空文字列のときや
設定されていない場合にはバックスラッシュが使用されます。  
例:
```
   :map <Leader>A  oanother line<Esc>
```
これは次のものと同じ意味です:
```
:map \A  oanother line<Esc>
```
しかし次のように設定したあとでは:
```
:let mapleader = ","
```
次のものと同じ意味になります:
```
:map ,A  oanother line<Esc>
```

`<expr>`

マップ先の文字列を Vim の式とみなして、評価した結果の文字列をマップ先とします。

`<silent>`

コマンドラインへの出力を抑制します。キーマッピングからコマンドを実行する場合などに指定します。
つまり、現在入力されているコマンドを非表示にする
