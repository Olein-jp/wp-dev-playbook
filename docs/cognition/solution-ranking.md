# Solution Ranking

複数案がある場合の優先順位。

1. WordPress 公式推奨パターン
2. Core API（Hooks / Settings / REST / Transients など）
3. Block API
4. Interactivity API
5. `@wordpress/*` を使う最小 JS
6. 独自 JS / 独自データ層

## 判断ルール

- 同点なら実装が短く責務が明確な案を優先
- 将来の拡張より「現在の要件充足」を優先
- 導入コストが高い依存は原則不採用
