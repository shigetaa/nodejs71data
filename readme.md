# データの活用方法について
クロールして得たデータを活用する時に考えられるのが「予測」と「分類」と「関連」です。
データを幅広く活用する方法について考察していきます。

## データをどのように活用するか？
収集したデータをどのように活用して行くのかを紹介していきます。

## データマイニングしよう
データマイニングとは、大量のデータを調べて、そこから価値のある情報を抽出する事を言います。
特に、今まで知られていなかった情報を、大量のデータの中から抽出する事、またその技術体系を指してます。
データを調べる方法には、統計学、パターン認識、人口知能など、データ解析の技法を利用します。

そもそも、マイニングとは採鉱と言う意味です。
広い鉱山から隠された金脈を採掘するのと同じように、大量のデータを解析する事で価値のある情報を見つける事が、データマイニングです。

データマイニングの中で特にテキストを対象とするものを
「テキストマイニング」、Webページを対象にしたものを「Webマイニング」と呼びます。

## データマイニングの基本は「予測」「分類」「関連」
データマイニングが難しいのは、ただデータを入れれば結果が出るというものではないという点にあります。
大量のデータの中から知識の発見を行う必要があります。
そのために必要なのが、仮説を立てることです。
マーケティングで言えば、その仮説は「予測」「分類」「関連」から考えることが出来ます。

### 「予測」について
そもそも「予測」とは、将来の出来事や有様を何らかの根拠に立って推し測る事です。
似た言葉に「予想」という言葉がありますが、予測が予想と違うのは、それが当てずっぽうではなく、
何らかしらの根拠に基づいているというてんです。

一般的に言って予測をする時には、その事象が発生する確率を算出する事になります。

### 「分類」について
「分類」とは、複数の物事や現象を何らかの基準に従って区別することによって体系づけることを言います。
分類する事で、情報を整理する事ができ、物事を把握しやすくなり多くのメリットがあります。

例えば、図書館における蔵書の整理を考えてみましょう。
膨大な蔵書を分類し整理する事で、利便性があがり読者は本を見つけやすくなります。

正しく分類を行うことで、様々な仮説を考えることが可能になります。

例えば、目の前に漠然とした顧客データがあるとします。
どんな分類ができるでしょうか。
- 男性と女性に分ける
- 20代、30代、40代など年代で分ける
- 年収で分ける
- 職種で分ける
- 購入した商品の色で分ける
- 購入した金額で分ける

この様に、同じ顧客データにしても、様々な分類が可能です。
違う分類を組み合わせて赤色の商品を買う人は、年収が高く、当社の高級な商品をよく買っているなどと、仮説を立てることができます。

### 「関連」について
「関連」とは、ある事柄と事柄との間につながりがあることを言います。
データベースに蓄積されたデータを調べることで、頻繁に同時に起きる事象を見つけることができる可能性があります。

例えば、スーパーの販売データを調べたところ、、おむつを買う人はビールも同時に購入する。
雨の日は肉の売り上げが上がる、など、データを調べることで思わぬ発見があります。
こうした情報を活かしていくことで、売上を伸ばすことが出来ます。

## データマイニングの手順
データマイニングのやり方をまとめると、以下の様になります。

1. 対象データを収集
2. 形態素解析などしてデータを分割
3. データをクリーニング（外れ値、欠損値、ノイズ除去）
4. データを要約（次元縮約、属性選択など）
5. データマイニング（統計や他のデータと組み合わせるなど）
6. 評価と検証

## 代表的なデータマイニング手法
データマイニングを行う際には、以下ような手法が考えられます。

1. 相関ルール：Xが起きるときにはYも起きやすい
2. 回帰分析：Xの属性から、数値変数Yを予測
3. クラス分類：Xの属性から、そのクラスCを予測
4. クラスタリング：似ている者同士をまとめる

詳しく説明します。

1. 相関ルールは、アソシエーションルール抽出とも言います。
   代表的な用途は、小売業のＰＯＳシステムです。
   例えば、コンビニで「パンと野菜ジュースを買う人は、ヨーグルトも一緒に買う」などの分析を行うことを言います。
2. 回帰分析は、相関関係や、因果関係があると思われる２つの変数のうち、一方の変数から将来的な値を予測するための予測式を求めるための手法です。
   データの傾向を分析することで、予測を行うことが出来ます。
3. クラス分類とは、特定の分類法をより正確に再現するモデルを作成することが目的です。
   方程式や、ルール、確率、マッチングなど、様々な手法が考えられます。
4. クラスタリングは、でーたの集合を部分集合（クラスタ）に切り分けて、それぞれの部分集合に含まれるデータがある共通の特徴を持つようにすることです。
   この特徴は、多くの場合、類似性やある定められた距離尺度に基づく近さで示されるものです。


# ベイジアンフィルタによる分類
ここでは、ベイジアンフィルタによる分類について解説します。
ナイーブベイズ分類を利用して、自動的に文章を任意のカテゴリに分類するプログラムを作っていきます。

## ベイジアンフィルタとは
ベイジアンフィルタは「ナイーブベイズ分類」を応用したもので、対象となるデータを解析・学習し分類する為のフィルタです。
身近な所では、迷惑メールを識別するフィルタの仕組みとして広く知られている機械学習処理のアルゴリズムです。
学習量が増えるとフィルタの分類精度が上昇するという特徴を持っています。

例えば、迷惑メールかどうかを判定するプログラムは、迷惑メールに使われている語彙を学習し、新たに来たメールでどのような語彙が使われているかを調べて、迷惑メールかどうかを判定します。
もし、判定を間違えた場合には、ユーザーが迷惑メールである事を学習させることで、より精度が高くなります。
迷惑メールかどうかを判定する部分に使われているアルゴリズムが、ベイジアンフィルタです。

従来型のキーワード指定によるフィルタでは、ユーザーが一つ一つＮＧワードを入力することで、迷惑メールを判定していました。
しかし、ベイジアンフィルタは、対象データの内容をフィルタが学習して自動的に分類する為、ユーザーが煩雑なキーワード指定を行う必要がありません。

このように、迷惑メールの判定で有名になった「ベイジアンフィルタ」ですが、他にも文章のカテゴリー分けに利用することが可能です。

## ナイーブベイズ分類のアルゴリズム
それでは、ベイジアンフィルタ、つまり、ナイーブベイズ分類のアルゴリズムについて簡単に紹介します。

ナイーブベイズ分類器というのは、ベイズの定義を利用した分類手法です。
ベイズ定義と言うのはつぎのような物です。

### ベイズの定義
入力`X`が与えられたとき、出力`Y`が得られる確率を`P(Y|X)`と表します。
そして、これをベイズの定義で表すと以下の様になります。

<img src="https://latex.codecogs.com/svg.image?P(Y|X|)&space;=&space;\frac{P(Y)P(X|Y|)}{P(X)}" title="P(Y|X|) = \frac{P(Y)P(X|Y|)}{P(X)}" />

