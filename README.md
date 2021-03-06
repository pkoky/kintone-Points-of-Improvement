# kintone【不具合•改善点】
<br>

## 今回書く理由
　kintoneを無料期間で使ってみたところ、とても使いやすく多くの人が必要とするアプリケーションだと感じました。ユーザーの視点から気になった部分があったので、更にいい製品にするための役に立てればと思い、感じたことをまとめることにしました。すでに把握されていて織り込み済みのものばかりであれば申し訳ございません。
 
<br>


### 目次
> #### 不具合　
> 1. ヘルプをクリックによる再表示ができない  
> 2. ２本指でスクロールした時の挙動  
> 3. 非同期通信による件数の変化がされない  

> #### 改善点
> 1. スマートフォンでのログインフォームが小さいと感じる  
> 2. 数字入力が暗黙的になっている


<br>

# 不具合
<br>

## 1. ヘルプをクリックによる再表示ができない
- アプリの設定画面で「計算」「スペース」フィールドの設定で使われているヘルプマークをクリックでオープン＆クローズすると2度目のオープンができない。
- マウスを移動させた後に、オープン可能となる。

https://user-images.githubusercontent.com/78239360/156074181-61a6cfa6-e043-4c99-ac7a-4a1b7ed5df0e.mov

***
<br>

## 2. ２本指でスクロールした時の挙動
- 既存のアプリの説明ページで、スクリーンショットを選択し、二本指でスクロールをするとすごいスピードで画像が切り替わることが繰り返される。バグではないが、バグと勘違いしてしまい驚いてしまう人がいそう。

*アプリ説明ページ*

https://user-images.githubusercontent.com/78239360/156075895-4a837db1-e68a-4385-8468-1c3f311a1ab3.mov

***

### 提案
- スクロールでの挙動をなくし、方向キーのみで動作するように修正でも使用者側としては問題ないかもしれないです。

***
<br>

## 3. レコード削除の際、レコード件数が非同期で変更されない
- アプリのレコードを削除した際に、レコード件数が非同期で変更されない。
- リロードをすると変更される。
- 本当に消せているか不安に思う人がいるかもしれない。

https://user-images.githubusercontent.com/78239360/156085829-78512c8e-26d0-4e7a-8e42-0ebe7b575e1d.mov

***
<br>

# 改善点
<br>

## 1.スマートフォンでのログインフォームが小さいと感じる
- アイフォンから見るブラウザのログインページが小さく感じる。妻に使ってもらった際、第一声で「これ小さいね」と言っていた。
- iPhone12では画面が少し大きいためあまり不具合を感じなかったが、妻はiPhoneXSを使っていて確かに小さかった。画面サイズの小さいスマートフォンだとさらに小さく感じられると思う。
- kintoneを使い始める際に最初に開く可能性の高いページであり、この段階でわかりずらいと感じてしまうとアプリケーション自体に悪印象を抱いて使い始められる心配がある。
<p align="center">
  <img src="https://user-images.githubusercontent.com/78239360/156076886-253380ad-e16c-47f2-b8e9-ff24749d9fe2.jpeg" alt="altテキスト" width="400px">
</p>

***

<br>

## 提案
- スマートフォンの場合は画面幅いっぱいに広げ文字サイズも大きくすると、ご高齢の方などより幅広いユーザーが使いやすくなるかもしれないです。
<p align="center">
  <img src="https://user-images.githubusercontent.com/78239360/156081671-4348ba0e-1444-4464-a2f6-a9de71a67fc1.jpeg" alt="altテキスト" width="400px">
</p>

***

## 2. 数値フィールドが暗黙的になっている
- 数値フォームに全角の数字を入れると「数字でなければなりません。」と表示される。
- パソコンに慣れていない人は全角•半角どちらも同じ数字だと捉えられると思う。エラー分の意味がわからない可能性がある。

<img width="1143" alt="スクリーンショット 2022-03-01 8 42 49" src="https://user-images.githubusercontent.com/78239360/156078204-d6398510-572b-454c-84e5-edd6c2a6bc64.png">
　
 ***
 
 <img width="694" alt="スクリーンショット 2022-03-01 8 51 03" src="https://user-images.githubusercontent.com/78239360/156078487-30c9cfc8-e9f4-43ae-856c-35a64f23b3bf.png">


***

## 提案
- エラー文を「半角数字」に修正するか、placeholderで半角数字と設定するといいかもしれないです。
- 全角数字を半角数字に変換する。（これが一番親切かもしれませんが、処理の負荷も考えた場合、エラー文の修正かplaceholderに設定するだけでいいのかもと個人的には思いました）

***


