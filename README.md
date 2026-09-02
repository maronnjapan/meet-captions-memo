# 字幕メモ (Meet Captions Memo) — review-markdown-cli へ移動しました

このリポジトリで開発していたChrome拡張機能は、
**[review-markdown-cli](https://github.com/maronnjapan/review-markdown-cli) の `extension/` へ移りました。**
以後の開発・issue・pull requestは、そちらでお願いします。

- 拡張機能の本体: <https://github.com/maronnjapan/review-markdown-cli/tree/main/extension>
- 使い方: <https://github.com/maronnjapan/review-markdown-cli/blob/main/extension/README.md>
- CLIとの連携: review-markdown-cli の README「Google Meetの字幕をリアルタイムで取り込む」

## なぜまとめたか

この拡張機能は、単体では「字幕をブラウザのローカル領域へ溜める」ところまでしかしません。
記録が使える形になるのは、review-markdown へ流し込んで、そこでAIに読ませてからです。
繋ぎ目（トークン・エンドポイント・連携コードの形式）は両側で揃っている必要があり、
片方だけ直すと黙って繋がらなくなります。一緒に直すものは、一緒に置いておくべきでした。

まとめたついでに、繋ぐ手順も短くしました。以前はURLとトークンを別々に手で打ち込んで
いましたが、いまは連携コードを1本貼るだけです。

## これまでの履歴

このリポジトリのコミット履歴は、review-markdown-cli 側へ `extension/` として取り込んであります
（subtreeマージ）。移動前のコードを読みたいときは、このリポジトリの過去のコミットか、
review-markdown-cli の履歴のどちらからでも辿れます。

## 使い方（移動先の要約）

```bash
# 拡張機能フォルダの場所を出す
review-markdown extension

# chrome://extensions でデベロッパーモードをオンにし、
# 「パッケージ化されていない拡張機能を読み込む」でそのフォルダを選ぶ
```

review-markdown を起動し、画面右上の「Meet連携」に出る**連携コード**を、
拡張機能のポップアップへ貼れば繋がります。
