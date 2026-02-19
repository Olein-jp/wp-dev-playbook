# 実装記録サンプル（1タスク分）

## タスク

投稿編集画面に「画像 alt 未設定」チェックを追加する。

## 1. Design Before Code

- 目的: 公開前に alt 未設定画像を検出し、編集者へ警告する
- 対象ファイル:
  - `includes/checks/class-alt-check.php`
  - `build/editor-sidebar.js`
- 影響範囲: 管理画面の投稿編集 UI のみ
- 採用する WordPress API:
  - `add_action( 'save_post', ... )`
  - `current_user_can()`
  - `wp_verify_nonce()`
- 代替案を却下した理由:
  - 正規表現のみ解析案は誤検知率が高く却下

## 2. 最小実装定義

- 今回「作らない」もの: 自動で alt を補完する機能
- 今回の完了条件: 未設定画像数と対象 URL を警告表示できる
- 追加リファクタ対象: 既存チェックの共通レスポンス整形

## 3. Refactor Loop 実施

- 重複していたレスポンス整形を `normalize_check_result()` に統一
- 条件分岐を早期 return へ変更し、ネストを 3 -> 1 に削減

## 4. Review Flow

- WordPress: Core API のみで実装し、独自 DB 操作なし
- Security: nonce / capability を保存処理前に検証
- Accessibility: 警告 UI をリスト化し、キーボード到達可能
- Performance: 追加クエリなし、既存 HTML 解析結果を再利用
- 可読性: 関数責務を「検出」「整形」「表示」に分離

## 5. Definition of Done 判定

- [x] `PROJECT.md` の要件に一致
- [x] スコープ外機能を含まない
- [x] sanitize / validate / escape を適用
- [x] キーボード操作と Focus 可視を満たす
- [x] 不要クエリ・不要 JS なし
- [x] 最低 1 回のリファクタ実施

## 6. Final Gate

- [x] Architect OK
- [x] Builder OK
- [x] WordPress Reviewer OK
- [x] Accessibility Reviewer OK
- [x] Performance Reviewer OK
- [x] Definition of Done を満たす
