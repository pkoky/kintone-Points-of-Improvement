# kintone【バグ•改善点】
<br>

### 目次
> #### バグ　
> 1. ヘルプの再表示エラー  
> 2. ２本指でスクロールした時の挙動  
> 3. 非同期通信による件数の変化がされない  

> #### 改善点
> 1. スマートフォンでのログインフォームが小さい  
> 2. 数字入力が入力が明示的でない  
> 3. レコード編集アイコンなどが初心者に何をするボタンか理解できない
> 4. アプリの新規作成途中で画面遷移をした際に、何もないアプリが作成される。  
<br>

# バグ
<br>

## 1. ヘルプの再表示エラー 
- アプリの設定画面で「計算」「スペース」フィールドの設定で使われているヘルプマークをクリックでオープン＆クローズすると2度目のオープンができない。
- マウスを移動させた後に、オープン可能となる。

https://user-images.githubusercontent.com/78239360/156074181-61a6cfa6-e043-4c99-ac7a-4a1b7ed5df0e.mov

***

### 提案
- boolean値によってオープンクローズを管理しているのであれば、クローズの際にboolean値も変更される修正をすると直ると思います。
- クリックでクローズ出来ないようにして、マウスを移動させたときにのみクローズされるようにするのも一つの案かもしれません。
- クリックではなくホバー時に表示されるようにする。（表示したくない時も表示されてしまいますが。。。）

***
<br>

## 2. ２本指でスクロールした時の挙動
- 既存のアプリの説明ページで、スクリーンショットを選択し、二本指でスクロールをするとすごいスピードで画像が切り替わることが繰り返される。バグではないが、バグと勘違いしてしまい驚いてしまう人がいそう。
- アプリに登録済みのレコードの添付ファイルで写真を開いた際にも同じ挙動が起こる

*アプリ説明ページ*

https://user-images.githubusercontent.com/78239360/156075895-4a837db1-e68a-4385-8468-1c3f311a1ab3.mov

***

*レコードの添付ファイル*

https://user-images.githubusercontent.com/78239360/156075206-34c413e1-7914-433f-9225-15fd5767ba84.mov

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

## 1.スマートフォンでのログインフォームが小さい
- アイフォンから見るブラウザのログインページが小さく感じる。妻に使ってもらった際、第一声で「これ小さいね」と言っていた。
- iPhone12では画面が少し大きいためあまり不具合を感じなかったが、妻はiPhoneXSを使っていて確かに小さかった。画面サイズの小さいスマートフォンだとさらに小さく感じられると思う。
- kintoneを使い始める際に最初に開く可能性の高いページであり、この段階でわかりずらいと感じてしまうとアプリケーション自体に悪印象を抱いて使い始められる心配がある。
<p align="center">
  <img src="https://user-images.githubusercontent.com/78239360/156076886-253380ad-e16c-47f2-b8e9-ff24749d9fe2.jpeg" alt="altテキスト" width="400px">
</p>

***

<br>

## 提案
- スマートフォンの場合は画面幅いっぱいに広げて、文字サイズも大きくするとご高齢の方も使いやすくなるかもしれない。
<p align="center">
  <img src="https://user-images.githubusercontent.com/78239360/156081671-4348ba0e-1444-4464-a2f6-a9de71a67fc1.jpeg" alt="altテキスト" width="400px">
</p>

***

## 2. 数値フィールドが明示的でない
- 数値フォームに全角の数字を入れると「数字でなければなりません。」と表示される。
- パソコンに慣れていない人は全角•半角どちらも同じ数字だと捉えられると思う。エラー分の意味がわからない可能性がある。

<img width="1143" alt="スクリーンショット 2022-03-01 8 42 49" src="https://user-images.githubusercontent.com/78239360/156078204-d6398510-572b-454c-84e5-edd6c2a6bc64.png">
　
 ***
 
 <img width="694" alt="スクリーンショット 2022-03-01 8 51 03" src="https://user-images.githubusercontent.com/78239360/156078487-30c9cfc8-e9f4-43ae-856c-35a64f23b3bf.png">


***

## 提案
- placeholderで半角数字と設定しておくのが、早く修正ができて効果も高いと思います。
- 全角数字を半角数字に変換する。（これが一番親切かもしれませんが、処理の負荷も考えた場合、placeholderに設定するのがいいかもしれないです）

***

<br>

## 3. レコード編集アイコンなどが初心者に何をするボタンか理解できない
- レコードを編集したりするアイコンが何をするボタンなのかがわかりずらいと感じる。
- 特に使い始めの頃に、ICTに慣れていない人などは何が起こるかわからないからボタンを押すのが怖いと感じられると思う。

<img width="1728" alt="スクリーンショット 2022-02-28 14 56 41" src="https://user-images.githubusercontent.com/78239360/156078796-33b6beab-8d8e-4392-8293-224bc3400a9a.png">

## 提案
- マウスホバー時に言葉の説明が表示されるとわかりやすいと思います。

https://user-images.githubusercontent.com/78239360/156082919-c5a254ed-36f6-46cd-ad22-377256a786d2.mov

***
<br>

## 4. アプリの新規作成途中で画面遷移をした際に、何もないアプリが作成されている
- アプリの「はじめから作成」ボタンを押し、「作成を中止」を押さずにホームボタンなどによって画面遷移をした場合、何もないアプリが作成されている。
- アプリ一覧では表示されないが、アプリ管理画面で見ると表示されている。
- 知らない間に不要なアプリが溜まってしまい、アプリ管理が煩雑になってしまう心配がある。
- アプリ作成途中で誤って画面遷移をしてしまった時のリスクヘッジになっている。

<img width="1693" alt="スクリーンショット 2022-03-01 10 26 34" src="https://user-images.githubusercontent.com/78239360/156091956-f90fab6e-6841-40c9-af60-9a63fdd686d9.png">

## 提案
- 何も追加などされていない場合は保存されないようにしてはどうでしょうか。
- アプリ作成画面で画面遷移をしようとした際、「作成を中止」を押した時のアラートが出るようにするのもいいかもしれません。
