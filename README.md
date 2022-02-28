# kintone【バグ•改善点】

### 目次
1. ヘルプの再表示エラー  
2. ２本指でスクロールした時の挙動  
3. 非同期通信による件数の変化がされない  
4. スマートフォンでのログインフォームが小さい  
5. 数字入力が入力が明示的でない  
6. レコード編集アイコンなどが初心者に何をするボタンか理解できない  

## バグ
**1.　ヘルプの再表示エラー** 
- アプリの設定画面で「計算•スペース」の項目の設定で使われているヘルプマークをクリックでオープン＆クローズすると2度目のオープンができない。
- マウスを移動させた後に、オープン可能となる。

https://user-images.githubusercontent.com/78239360/156074181-61a6cfa6-e043-4c99-ac7a-4a1b7ed5df0e.mov

***

**2.　２本指でスクロールした時の挙動**
- 既存のアプリの説明ページで、スクリーンショットを選択し、二本指でスクロールをするとすごいスピードで画像が切り替わることが繰り返される。バグと思ってしまう人が多そう。
- アプリに登録済みのレコードの添付ファイルで写真を開いた際にも同じ挙動が起こる

*アプリ説明ページ*

https://user-images.githubusercontent.com/78239360/156075895-4a837db1-e68a-4385-8468-1c3f311a1ab3.mov

***

*レコードの添付ファイル*

https://user-images.githubusercontent.com/78239360/156075206-34c413e1-7914-433f-9225-15fd5767ba84.mov


***

**3.　非同期通信による件数の変化がされない**
- アプリのレコードを削除した際に、件数が非同期で変わらないため、ユーザーが混乱する可能性がある。

https://user-images.githubusercontent.com/78239360/156076469-2e093855-1fdf-4024-a0f3-08ea7a74e759.mov

***

**4.　スマートフォンでのログインフォームが小さい**
- アイフォンから見るブラウザのログインが小さく感じる。妻使ってもらった時に第一声で「これ小さいね」と言っていた。
- 妻はiPhoneXSを使っていて確かに小さかった。iPhone12では画面が少し大きいため少しましに感じる。
<p align="center">
  <img src="https://user-images.githubusercontent.com/78239360/156076886-253380ad-e16c-47f2-b8e9-ff24749d9fe2.jpeg" alt="altテキスト" width="400px">
</p>

***

**5.　数字入力が入力が明示的でない**
- 数値フォームに全角の数字を入れると「数字でなければなりません。」と表示される。パソコンに慣れていない人だと、「数字だけど？」と思ってしまいそう。明示的に「半角数字入力」など書くとわかりやすそう。



<img width="1143" alt="スクリーンショット 2022-03-01 8 42 49" src="https://user-images.githubusercontent.com/78239360/156078204-d6398510-572b-454c-84e5-edd6c2a6bc64.png">
　
 ***
 
 <img width="694" alt="スクリーンショット 2022-03-01 8 51 03" src="https://user-images.githubusercontent.com/78239360/156078487-30c9cfc8-e9f4-43ae-856c-35a64f23b3bf.png">
