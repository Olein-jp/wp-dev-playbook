# Definition of Done

## 1. 設計

- [ ] `docs/PROJECT.md` の対象要件に一致している
- [ ] スコープ外の実装を含まない

## 2. WordPress 品質

- [ ] WordPress 標準 API を優先している
- [ ] Coding Standards に反しない
- [ ] Hook / 責務分離が妥当

## 3. Security

- [ ] sanitize / validate / escape が適切
- [ ] nonce / capability チェックが適切

## 4. Accessibility

- [ ] セマンティック構造が成立している
- [ ] キーボード操作と Focus 可視を満たす

## 5. Performance

- [ ] 不要クエリ・不要 JS がない
- [ ] 実装前後の性能観点を説明できる

## 6. 保守性

- [ ] 命名と責務が明確
- [ ] 最低 1 回のリファクタを実施
