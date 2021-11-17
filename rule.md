## omotebako-sequenceを作る目的
どのマイクロサービスでどのようなロギングがされているかを把握することを目的とする。
そのため、一般的なシーケンス図とは異なり、ロギングに関しては細かい処理についても図に記入する

## mermaid 書き方のルール

1.抽象度の高い内容はMessagesへ
2.具体的な処理内容（関数, ロギング, キュー名）はNoteに記入する
3.処理内容を書く際には以下の接頭辞をつける
- 関数:    　func
- ロギング: 　logger メッセージのみ表記
- 例外発生: error
- キュー:  　 queue
- API:   　 　api
- 画面遷移: 　router
- 別紙参照：   ref
4. 処理落ちなどのビジネス上重要でないログは書かない

例外処理の書き方
```
alt 例外発生
    hogehoge
```
5. 重要なメッセージはrectで色付けする

## その他
- [mermaidチートシート](https://mermaid-js.github.io/mermaid/#/sequenceDiagram?id=sequence-diagrams)

## 注意
マイクロサービス名としてハイフン（-）を使うことがありますが、marmaidではハイフンが特殊文字として認識され使えませんのでご注意ください。

