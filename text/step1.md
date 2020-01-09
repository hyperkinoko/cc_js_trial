# 序章のトレーニング

序章の課題``0-6``はできましたか？

HTMLファイルの中に、

```html
<script>
    alert('表示したい文字列');
</script>
```

と書くと、「表示したい文字列」と書かれたポップアップが出ますね。

## 序章の補足

### console.log()

alertとは別の、便利な出力を知っておきましょう。

```html
<script>
    console.log('表示したい文字列');
</script>
```

これを実行しても、画面は真っ白のままです。  
どこに出力されたのでしょうか？

「別タブ」をクリックして、ブラウザ画面を右クリック→「検証」と進み、右側に表示されたデバッグツールの「Console」というタブを開いてみてください。  
``console.log('表示したい文字列');``の出力は、ここに表示されます。

何行目のプログラムでこの出力が行われたのかもわかります。

また、エラーが発生している場合は、赤字でその内容が出力されます。  
「思ったとおりに動いていないな」というときは、必ず「検証」→「Console」を確認しましょう。

詳しいことは、教科書「Chrome デベロッパーツールの使い方」を読んでください。

### document.write()

``alert``は、ポップアップが表示され、OKが押されるまでプログラムが止まってしまいます。  
``console.log``は画面には表示されません。  
javascriptを使って、何かを画面に表示したいときはどうするのかというと、``document.write()``を使います。  
（もっといい方法はたくさんありますが、現時点ではこれがベストです。）

``document.write()``はHTMLに直接文字を書き出すことができます。
HTMLに書き出すので、その内容はもちろんHTMLでないといけません。

だめな例：

```html
<script>
    document.write('表示したい文字列');
</script>
```

よい例：

```html
<script>
    document.write('<p>表示したい文字列</p>');
</script>
```

実際に両方のコードを書いて、「検証」→「Elements」で確認してみてください。
よい例のほうは、``<p>``要素としてきちんと出力されていますが、悪い例のほうは、不完全なHTMLになってしまっていますね。

## トレーニング1

``console.log``を使って、Consoleに「Hello World」と表示してください。

### チェックポイント

* 「検証」→「Console」にHello Worldと表示されていますか？

### サンプルコード

```html
<script>
    console.log('Hello World');
</script>
```

## トレーニング2

``document.write``を使って、画面に「Hello World」を ``<h1>``要素として出力してください。  

### チェックポイント

* 画面には大きな太文字で、「Hello World」と表示されている。

### サンプルコード

```html
<script>
    document.write('<h1>Hello World</h1>');
</script>
```

## トレーニング3

``document.write``を複数回使って、以下のようなHTMLを出力してください。

```html
<h1>Hello World</h1>
<p>こんにちは、世界！<br>javascriptはとても楽しいですね！</p>
<p>しっかり身につけましょう！</p>

```

### チェックポイント

* 画面には大きな太文字で、「Hello World」と表示されている。
* 「こんにちは、世界！」の後で改行されている。
* 段落と段落の間に隙間が空いている。

### サンプルコード

```html
<script>
    document.write('<h1>Hello World</h1>');
    document.write('<p>こんにちは、世界！<br>javascriptはとても楽しいですね！</p>');
    document.write('<p>しっかり身につけましょう！</p>');
</script>
```
