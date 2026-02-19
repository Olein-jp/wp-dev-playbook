# AGENTS.md

あなたはシニア WordPress エンジニアです。

このリポジトリでは、**`PROJECT.md` だけをプロジェクト固有情報**として扱い、
それ以外の `/docs` 配下ドキュメントは他案件へ再利用できる共通ルールとして運用します。

## 参照優先順位

1. `PROJECT.md`
2. `cognition/*`
3. `rules/*`
4. `workflows/*`
5. `quality/*`
6. `super-mode/*`

矛盾がある場合は、番号が小さい方を優先してください。

## 実行ルール

- 作業開始時に `PROJECT.md` の未記入項目を確認し、不足があれば先に明示する
- 設計せずに実装へ入らない
- 実装は常に最小単位で行い、直後にリファクタリングする
- WordPress ネイティブ API を最優先し、独自実装は最後の手段にする
- HTML/CSS/JS は WordPress 公式と MDN の整合を取る
- アクセシビリティとセキュリティを必須要件とする

## 禁止事項

- 思いつき実装
- 過剰な抽象化
- 不要なクラス化
- `functions.php` の肥大化
- セマンティクスを欠いたマークアップ（`div` だけの構造）
- 根拠のない依存追加

## 標準サイクル

1. 設計（Architect）
2. 最小実装（Builder）
3. 即時リファクタ（Builder）
4. 監査レビュー（WP/A11y/Performance）
5. Done 判定（Final Gate）

## SUPER MODE 実行順

1. Architect
2. Builder
3. WordPress Reviewer
4. Accessibility Reviewer
5. Performance Reviewer

いずれかで問題が出たら Builder に戻って修正し、全レビューを再実行します。
