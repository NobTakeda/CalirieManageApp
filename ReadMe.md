###カロリー管理アプリ### 

既知の不具合) 
・まだ献立を登録していない日を指定して 
「この日食べたものを見る」ボタンを押すと落ちますのでご注意ください 

・「献立を登録する」ボタンを押した後に「献立を更新する」ボタンが出てまいりますが、 
「更新する」ボタンを2回以上押すとブラウザが止まりますのでご注意ください 

・色々修正してたらグラフ表示ページで戻るボタンを押すと落ちるようになってましたごめんなさい 

contextのパスワードは空になっておりますので、ユーザー様ごとに
自分のデータベースへ接続できるよう書き換えてお使いください。

用意していただくデータベース情報
```
CREATE DATABASE mycalapp
DEFAULT CHARACTER SET utf8;
```
```
CREATE TABLE foods(
id INT PRIMARY KEY AUTO_INCREMENT,
name VARCHAR(30),
cal INT,
time_id INT,
updated DATE
);
```
```
CREATE TABLE fod(
id INT PRIMARY KEY AUTO_INCREMENT,
breakfastCal INT,
lunchCal INT,
supperCal INT,
totalCal INT,
updated DATE UNIQUE
);
```

データベースを使用し、 

・日々の献立を登録 
・1日ごとの合計カロリーを登録 
・現在から1週間前までのカロリーをグラフで表示 

以上ができることを目標に作りました。 
大まかな動きは実装できましたが、スタイルが当たっておらず 
肝心のグラフ表示ページが上から下に羅列されるだけとなっております。 

完成形では、1日ごとに朝、昼、晩と色分けして 
とったカロリー分横に伸びる棒グラフを作り、 
日々の合計カロリーの推移が視覚的にわかりやすくするつもりです。 
