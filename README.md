# ActivityCompat RequestPermissions Trial
ActivityCompat#requestPermissions()を用いて、権限リクエストする方法の試行

このアプリの挙動としては、以下。
- (1)「スタート」ボタンの初回押下⇒「権限リクエスト」ダイアログ⇒「許可」の押下⇒「カメラ処理開始『可能』」メッセージ
- (2)「スタート」ボタンの初回押下⇒「権限リクエスト」ダイアログ⇒「許可しない」の押下⇒「カメラ処理開始『不可』」メッセージ
- (3)「許可」後「スタート」ボタンの押下⇒「カメラ処理開始『可能』」メッセージ
- (4)「許可しない」後「スタート」ボタンの押下⇒「権限リクエストの理由説明」ダイアログ⇒「権限リクエスト」ダイアログ（⇒(1),(2)）
- (5)「今後表示しないをチェックして許可しない」後「スタート」ボタンの押下⇒「詳細設定画面への誘導」ダイアログ

## 関連
権限リクエストする方法は、「ActivityCompat#requestPermissions()を用いる方法」以外にも、「registerForActivityResult()を用いる方法」があります。  
「registerForActivityResult()を用いて、権限リクエストする方法の試行」については、以下リポジトリを参照。  
[RegisterForActivityResultTrial](https://github.com/nobukihiramine/RegisterForActivityResultTrial)

補足）  
2021/12/1 現在、Fragment#requestPermissions()は、deprecatedとなっているが、ActivityCompat#requestPermissions()は、deprecatedとはなっていないので、「ActivityCompat#requestPermissions()を用いる方法」「registerForActivityResult()を用いる方法」はどちらも有効な方法。  
２つの方法に動作の違いはない。実装上も大きな違いはないが、  
「ActivityCompat#requestPermissions()を用いる方法」は、クラスメンバーに、リクエストコード定義が必要。  
「registerForActivityResult()を用いる方法」は、クラスメンバーに、リクエストランチャー定義が必要。

## Screenshots : スクリーンショット
<img src="images/screenshot_anim01.gif" width="240" alt="Screenshot"/>

## Requirements : 必要条件、依存関係
- Android Studio 2020.3.1 Patch3

## Author : 作者
Nobuki HIRAMINE : [http://www.hiramine.com](http://www.hiramine.com)

## License : ライセンス
```
Copyright 2021 Nobuki HIRAMINE

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

