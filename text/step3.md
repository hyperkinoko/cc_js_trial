# 2章のトレーニング

2章はif文です。
javascriptだけでなく、いろいろなプログラミング言語で共通している考え方です。
これもしっかりマスターしておきましょう。

## 課題のヒント

2章の課題はできましたか？

``rand``という変数に0〜9の乱数を代入しますね。

```
var rand = Math.floor(Math.random() * <乱数の上限値より1大きい数>);
```

しばらくはおまじないのように使ってください。
そのうち、Mathがクラスであることや、``floor()``や``random()``がMathクラスのメソッドであることも学習します。

出力は、``document.write``を使い、きちんとHTMLの形で（``<p>``要素など）出力しましょう。

偶数か奇数かは、「2で割った余りが0か1か」で分けられますね。

大きさを比べるときには、「<」や「>」、「<=」や「>=」を使います。  
if文の中にif文を入れたり、条件を複数合わせたりして、うまく最大のものを見つけてくださいね。

## トレーニング1

おみくじを作ってみてください。

1. nameという変数に名前を入れることができる。
2. 0〜100の乱数randを作り、以下のように結果（変数名：result）を設定する。

* 0〜15: 大凶
* 16〜35: 凶
* 36〜65: 小吉
* 66〜85: 吉
* 86〜100: 大吉

表示結果：

```html
<p>○○さんの今日の運勢は、大吉です</p>
```

また、randがどんな数字であったかも表示しましょう。  
ただし、こちらは、画面上ではなくConsoleに表示します。

### チェックポイント

* 名前が表示されている。
* 運勢が表示されている。
* 結果がHTMLとして出力されている。
* randの内容がConsoleに表示されている。おみくじの結果と整合している。

### サンプルコード

```js
var name = '松本';
var rand = Math.floor(Math.random() * 101);
var result = '';

if(rand > 85) {
    result = '大吉';
} else if(rand > 65) {
    result = '吉';
} else if(rand > 35) {
    result = '小吉';
} else if(rand > 15) {
    result = '凶';
} else {
    result = '大凶';
}

console.log(rand);
document.write('<p>' + name + 'さんの今日の運勢は、' + result + 'です</p>');
```

## トレーニング2

0〜100の乱数randを作り、3の倍数のときFizz、5の倍数のときBuzz、3と5の公倍数（3でも5でも割り切れる）のときFizzBuzzと表示しましょう。
3でも5でも割り切れないときは、そのまま数字を表示します。
また、Consoleには、乱数をそのまま表示しましょう。

### チェックポイント

* Fizz、Buzz、FizzBuzzが正しく表示されている。
* 結果がHTMLとして出力されている。
* randの内容がConsoleに表示されている。

### サンプルコード

```js
var rand = Math.floor(Math.random() * 101);

console.log(rand);

if(rand % 3 === 0 && rand % 5 === 0) {
    document.write('<p>FizzBuzz</p>');
} else if(rand % 3 === 0) {
    document.write('<p>Fizz</p>');
} else if(rand % 5 === 0) {
    document.write('<p>Buzz</p>');
} else {
    document.write('<p>' + rand + '</p>');
}
```
