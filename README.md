# transformer-research

transfomerを使って試したことをいろいろ記載します。

## 次元サイズの違いによる比較
モデル：transformer(エンコーダー6層、デコーダー6層)

学習データ：CC100-jaを切り出して作成した77MBのテキスト

学習タスク：再構成(入力と同じテキストを出力するタスク)

エポック：10

比較次元：256,512

![image](https://github.com/tsutsui-439f340f/transformer-research/assets/55880071/2c624d49-ab36-4e6a-be4f-12bd3189cc78)
![image](https://github.com/tsutsui-439f340f/transformer-research/assets/55880071/30ed0de5-f47e-4f13-83e1-5555e0e3c1dc)



## GPT-2(rinna/japanese-gpt2-medium)を使用してパラメータを一部固定したときの比較
モデル：GPT-2(デコーダー24層)

学習データ：小説データ1000テキスト

学習タスク：次単語予測

エポック：10

バッチサイズ：4

比較パラメータサイズ：(151156736(前半のモジュールを固定),184973312(モジュール2つおきに固定),260550656(モジュール5つおきに固定),オリジナル)


