# WordPress Standards

- WordPress Coding Standards 準拠
- 可能な限り Core API を優先
- Hook 設計を優先し、直接改変を避ける

## データ処理

- 入力: sanitize / validate
- 出力: context に応じて escape
- 権限: capability チェック必須
- 送信: nonce 検証必須

## 国際化

- 原則として i18n 対応を前提に実装
- 対象外にする場合は `PROJECT.md` に明記
