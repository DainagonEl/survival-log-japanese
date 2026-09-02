# トラブルシューティング

作業前にゲームとBepInExのコンソール画面を終了してください。

## 日本語にならない

次を確認してください。

- Release Noteに記載されたゲーム版と一致している
- 対応する日本語化MODを使用している
- BepInEx 6が正しく導入されている
- インストーラーがエラーなく完了した

解決しない場合は、ゲーム版、MOD版、`BepInEx\LogOutput.log`を添えて[不具合報告](https://github.com/DainagonEl/survival-log-japanese/issues/new/choose)を作成してください。

## インストーラーが対応外として停止する

ゲーム更新やファイルの不一致を検出しています。安全のため、手作業で上書きせず、表示されたメッセージとゲーム版を不具合報告へ添えてください。

## ゲームが起動しない

まず[導入方法](installation.md)の「削除して元に戻す」を実行します。その後、Steamの「ゲームファイルの整合性を確認」で元の状態へ戻し、ゲーム単体で起動できるか確認してください。

## 一部が英語のまま表示される

[未翻訳報告](https://github.com/DainagonEl/survival-log-japanese/issues/new/choose)から、表示場所とスクリーンショットをお送りください。

## 訳文や表示が不自然

[翻訳改善提案](https://github.com/DainagonEl/survival-log-japanese/issues/new/choose)から、現在の訳、希望する訳、表示場所をお知らせください。

## ログを添付するとき

`BepInEx\LogOutput.log`に個人情報や認証情報が含まれていないことを確認してください。必要な箇所だけを添付して構いません。
