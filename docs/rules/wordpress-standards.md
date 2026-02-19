# WordPress Standards

- WordPress Coding Standards 準拠
- 可能な限り Core API を優先
- Hook 設計を優先し、直接改変を避ける

## 機能追加・カスタマイズ時の最優先事項

- 新機能やカスタマイズは、まず WordPress 公式推奨の Hook / 関数 / API で実現可能かを確認する
- 実現可能な場合は独自実装より先に、公式推奨の実装手段を採用する
- 公式手段を採用しない場合は、理由を設計時に明記する

## データ処理

- 入力: sanitize / validate
- 出力: context に応じて escape
- 権限: capability チェック必須
- 送信: nonce 検証必須

## 国際化

- 原則として i18n 対応を前提に実装
- 対象外にする場合は `docs/PROJECT.md` に明記
