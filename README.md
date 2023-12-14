# 2023年後期「JavaScript基礎」授業課題

## 授業内コード
 1. 10月５日（木）はじめの一歩
 2. 10月5日（木）GitHubレポジトリ作成
 3. 10月12日（木）文字列の連結、変数、定数、複合演算子
 4. 10月19日（木）documentオブジェクトとDOM
 5. 10月26日（木）その他のdocumentの取得と挿入、イベント
 6. 11月2日(木)classlistといろんなイベント
 7. 11月9可
 8. 12月7日
 9. 12月14日：コールバック関数とアロー関数
 0. 関数引数

 ## 12月14日
  - コールバック関数
   - コールバック関数は、関数の引数に関数を当てる使い方。正直よくわからん
 - アロー関数
  - thisが使えん
   - https://zenn.dev/syus_study/articles/becc681ce52a4b  ←これ見てみよう

   - 関数の実行・関数名・関数の定義

 ## 12月07日
 - 関数
 - 引数

 ## 10月19日
 - コレクション
 - 繰り返し配列

 ## 配列の宣言と長さ

 ```js
 //fruitsの配列
const fruits = ["りんご", "もも", "バナナ"];
//配列要素の数
console.log(fruits.length); //3
console.log(fruits[2]); //バナナ
for (let i = 0; i < 4; i++) {
  console.log(`for文のサンプル：${i}`);
}
 ```
 - 授業で書いたコード
 ```js
 <!DOCTYPE html>
<html lang="ja">

<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>複数要素の追加</title>
    <meta charset="UTF-8" />
</head>

<body>
    <h1>人気フルーツ一覧</h1>
    <ul id="fruitslist" class="listbox__list"></ul>
    <script>
        //ulの中に果物一覧を一度にliで入れたい
        //配列fruitsを宣言・値を代入
        const fruits = ["りんご", "もも", "バナナ"];

        //バナナがほしい
        console.log(fruits[2]);

        //ulをJavaScript空間に引きずり込む
        const Element = document.querySelector("#fruitslist");
        console.log(element);

        //fruitsの要素数分だけfor分で回す
        for (let i = 0; i < fruits.length; i++) {
            //liを創出する
            const lilast = document.createElement("li")

            //liに値（果物→配列fruitsの中にある）を代入
            console.log(fruits[i]);//りんご・もも・バナナが取れる
            //創出したliの内容に果物を代入
            lilast.textContent = fruits[i];
            //element(※ul)の中の最後に追加
            element.appendChild(lilast);

        }
    </script>
</body>

</html>
 ```


 ## 10月12日

 - リテラルと演算子
 - 文字列の連結
 - 変数と定数
 - 複合演算子

 ### 文字列の計算

 ```js
 //文字列の連結
console.log("ABC" + "EFG");
console.log("円周率は" + 3.14 + "です。");//文字列 + 数値
console.log("計算結果：" + 123 + 456);//文字列 + 数値の計算
console.log(123 + 456 + "となりました");//数理の計算 + 文字列
console.log("計算結果：" + (123 + 456));//文字列 + 数値の計算
console.log("2" - 1);//文字列 - 数値
console.log("2" * 3);//文字列 - 数値
console.log("2" / 4);//文字列 - 数値
 ```

 ### 変数の宣言

 ```js
 let a; //変数の宣言  //
 a = 10;//値の代入 (数値型)
 console.log(a);

 a = "Hello"; //値の再代入（文字列型）
 console.log(a);
 ```

 ### 定数の宣言

 ```js
 const PI = 3.24;
 console.log(PI);

 //再代入
 //PI = 3.2415926535;
 //const PI;
 ```

 ### 複合演算子

 ```js
 //複合演算子
 let n = 5;
 n = n + 2;
  console.log(n);//7

  let n2 = 5;
  n2 += 2; //複合演算子　n2 = n2 +2と同じ
  console.log(n2);

  //インクリメント
  let n3 = 5;
   n3++; //インクリメント　１たす
    console.log(n3); //6
 ```

 ### リストを操作するDOM操作のスクリプト

 ```js
 //ulタグのリスト要素を取得
        const element = document.querySelector("ul");
        console.log(element);

        //selectorってCSSのセレクターなので
        const element2 = document.querySelector("#fruitslist");
        console.log(element2);

        //classも行ける？
        const element3 = document.createElement(".listbox__list");
        console.log(element3);

        //新しい要素を作る
        const lilast = document.createElement("li");
        console.log(lilast);

 ```

 ## 10 月 5 日

- インターネットの基本について理解する。
- Web の基本的な仕組みを理解する。
- Web サーバーの役割について理解する。
- 開発環境の構築
- JavaScript を書く場所

### JavaScript を書く場所

1. HTML ファイルの中
1. 外部 JS ファイルの中
1. ブラウザのコンソール

基本は、外部 JS ファイルを読み込むが、HTML 内に各場合は、`</body>`の上に書く。

```html
<!doctype html>
<html lang=ja>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>演習</title>
</head>
<body>
</script>
</body>
</html>
```

### フロントエンドロードマップ

フロントエンドエンジニアに必要なスキルの[ロードマップ](https://roadmap.sh/frontend)がある。
