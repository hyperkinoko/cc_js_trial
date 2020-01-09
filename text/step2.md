# 1章のトレーニング

1章は変数や演算など、javascriptのとても基本的で大切なことを学んでいます。  
しっかりマスターしておきましょう。

## トレーニング1-1

1章の課題``1-12``は実際に変数を表示してみましたか？  
まだの人はやってみましょう。

変数の中身を表示するには、``document.write()``や``console.log()``、``alert()``を使えばよかったですね。
今回は、変数の中身をしっかり確認したいので、``console.log()``を使ってみましょう。

### チェックポイント

* Consoleにそれぞれの変数が表示されている。
* 表示された内容が、予想と同じであった。

### サンプルコード

```html
<!--・・・HTML部省略-->
<script>
var q_1  = '1';
console.log(q_1);

var q_2  = 1;
console.log(q_2);

var q_3  = 'true';
console.log(q_3);

var q_4  = true;
console.log(q_4);

var q_5  = null;
console.log(q_5);

var q_6  = '';
console.log(q_6);

var q_7  = 'undefined';
console.log(q_7);

var q_8;
console.log(q_8);

var q_9  = 10 + '20';
console.log(q_9);

var q_10 = 10 + 10 + '20';
console.log(q_10);
</script>
```

## トレーニング1-2

上記の出力は、何行目の出力かはわかりますが、どの変数なのかイマイチ見にくいですね。

```
q_1: <q_1の中身>
q_2: <q_2の中身>
```

のように、どの変数を表示しているか、わかりやすくしてみましょう。

文字列と、変数の中身をつなげて表示するには、「+」を使います。
トレーニング1-1のコードを少し変えてみましょう。

### チェックポイント

* Consoleにそれぞれの変数が「q_1: xx」のように表示されている。

### サンプルコード

```html
<!--・・・HTML部省略-->
<script>
var q_1  = '1';
console.log('q_1: ' + q_1);

var q_2  = 1;
console.log('q_2: ' + q_2);

var q_3  = 'true';
console.log('q_3: ' + q_3);

var q_4  = true;
console.log('q_4: ' + q_4);

var q_5  = null;
console.log('q_5: ' + q_5);

var q_6  = '';
console.log('q_6: ' + q_6);

var q_7  = 'undefined';
console.log('q_7: ' + q_7);

var q_8;
console.log('q_8: ' + q_8);

var q_9  = 10 + '20';
console.log('q_9: ' + q_9);

var q_10 = 10 + 10 + '20';
console.log('q_10: ' + q_10);
</script>
```

## トレーニング2

変数に文字列を代入して、それを表示してみましょう。

1. nameという変数を作って、あなたの名前を代入しましょう。
1. 表示には``document.write()``を使い、画面に``<p>``要素として表示しましょう。
1. 「こんにちは、わたしは○○です」のように、あなたの名前がメッセージの中に組み込まれるようにしましょう。

### チェックポイント

* 「こんにちは、わたしは<あなたの名前>です」と表示されている。
* Elementsを確認すると、表示内容が``<p>〜</p>``で囲まれている。

### サンプルコード

```js
var name = '松本';
document.write('<p>こんにちは、わたしは' + name + 'です');
```

## 課題1-13、1-14の補足

まずは課題の1-13、1-14をやってみてください。
この2つの課題は、どちらも数字を演算した結果を表示しますね。
``document.write()``を使って、``<p>``要素として表示することにも注意してください。

演算の結果は、

```js
var apple = 100;
var grape = 150;

var goukei = apple + grape;

document.write('<p>合計： ' + goukei + '円</p>');
```

のように、一旦変数に置き換えてもOKです。

変数を増やさずに、直接表示することもできますが、

```js
var apple = 100;
var grape = 150;

document.write('<p>合計： ' + apple + grape + '円</p>');
```

この結果は、思ったような結果にはなりません。  
なぜか考えて、解決法を考えてみてくださいね。

わかった人は、答え合わせをしてみましょう。

```js
var apple = 100;
var grape = 150;

document.write('<p>合計： ' + (apple + grape) + '円</p>');
```

プログラムは前から順番に処理されるため、文字列とappleの中身（100）の「+」が先に処理され、「&lt;p&gt;合計: 100」という文字列が作られます。  
そのあとにgrapeの中身（150）が「+」されるので、これは文字列の連結として扱われます。

これを防ぐため、「apple + grape」の足し算（数字の四則演算）を先にしてくださいねという意味の``()``をつけてあげます。

課題1-14の四則演算も、``()``を上手に使って、処理の優先順を調整しましょう。

## トレーニング3

インクリメント演算子や代入演算子の省略形を使ってみましょう。

1. りんご1個の値段は130円です。（変数名: apple）
1. 個数（変数名: kosuu）の初期値は1に、合計（変数名: goukei）の初期値は0にします。
1. 1ずつ増やすのにはインクリメント演算子「++」を使ってみましょう。
1. 合計にりんご1個分の値段を追加するときには、省略形の代入演算子「+=」を使ってみましょう。
1. 1個ずつ増やしながら、5個まで、その個数と合計金額を表示してみましょう。  数行の処理を5回繰り返します。コピペでOKです。
1. 処理の順番に気をつけましょう。

表示結果：

```html
<body>
    <p>りんご1個： 130円</p>
    <p>りんご2個： 260円</p>
    <p>りんご3個： 390円</p>
    <p>りんご4個： 520円</p>
    <p>りんご5個： 650円</p>
</body>
```

### チェックポイント

* 結果が上記と同じになっている。
* 同じコードを使い回せている（for文の予習になります）
* Elementsを確認すると、表示内容が``<p>〜</p>``で囲まれている。

### サンプルコード

```js
var apple = 130;
var kosuu = 1;
var goukei = 0;

goukei += apple;
document.write('<p>りんご' + kosuu + '個： ' + goukei + '円</p>');
kosuu++;

goukei += apple;
document.write('<p>りんご' + kosuu + '個： ' + goukei + '円</p>');
kosuu++;

goukei += apple;
document.write('<p>りんご' + kosuu + '個： ' + goukei + '円</p>');
kosuu++;

goukei += apple;
document.write('<p>りんご' + kosuu + '個： ' + goukei + '円</p>');
kosuu++;

goukei += apple;
document.write('<p>りんご' + kosuu + '個： ' + goukei + '円</p>');
kosuu++;
```
