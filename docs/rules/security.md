# Security

## 必須チェック

- [ ] 全入力の sanitize / validate
- [ ] 全出力の escape
- [ ] 状態変更処理に nonce
- [ ] 実行権限の capability チェック
- [ ] 外部リクエストのタイムアウト / エラー処理

## 禁止

- 生 SQL の組み立て
- 認可前の更新処理
- ユーザー入力の未検証保存
