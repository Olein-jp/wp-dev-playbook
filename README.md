# wp-dev-playbook

WordPress テーマ/プラグイン開発の品質を安定化するための、運用ドキュメントセットです。  
ルートの `AGENTS.md` を入口に、`docs/` 配下の規約・フロー・品質基準を参照して開発します。

## 1. 何のためのリポジトリか

- 設計なし実装を防ぐ
- WordPress 公式推奨の Hook / 関数 / API を最優先で使う
- Security / Accessibility / Performance を実装時点で担保する
- レビュー観点と Done 条件を統一する

## 2. ディレクトリ構成

- `AGENTS.md`
  - エージェント向けの最上位運用ルール
- `docs/PROJECT.md`
  - プロジェクト固有情報（唯一の固有ファイル）
- `docs/cognition/`
  - 設計・思考モデル
- `docs/rules/`
  - 実装規約（WP / Security / A11y / Performance など）
- `docs/workflows/`
  - 開発・レビュー手順
- `docs/quality/`
  - Done 判定
- `docs/super-mode/`
  - 役割ベースレビュー
- `docs/example/`
  - 記入例（書式確認用。実装判断の根拠には使わない）
- `docs/logs/work-log.md`
  - 単一の作業ログ（追記式）

## 3. 最初にやること

1. `docs/PROJECT.md` を記入する
2. `AGENTS.md` の参照順と実行ルールを確認する
3. `docs/workflows/development-flow.md` に沿って着手する

## 4. 日々の使い方（基本）

1. 要件確認
   - `docs/PROJECT.md` のスコープ内か確認
2. 設計
   - `docs/cognition/design-before-code.md` を埋める
3. 実装
   - `docs/rules/wordpress-standards.md` を優先
   - まず WordPress 公式推奨手段（Hook / 関数 / API）を検討し採用
4. リファクタ
   - `docs/cognition/refactor-loop.md` を実施
5. レビュー
   - `docs/workflows/review-flow.md` と `docs/super-mode/review-cycle.md` を実施
6. 完了判定
   - `docs/quality/definition-of-done.md` と `docs/super-mode/final-gate.md` を満たす

## 5. 作業ログ運用

- ログは `docs/logs/work-log.md` の**1ファイル**に追記する
- 各エントリに以下を必ず記載する
  - 日付（`YYYY-MM-DD`）
  - 時刻（`HH:MM`）
  - 作業種別
  - 対象ファイル
  - 作業内容
  - 結果

## 6. 参考

- 記入例: `docs/example/PROJECT.example.md`
- 実装記録例: `docs/example/IMPLEMENTATION-RECORD.example.md`

