# Anti Patterns

## WordPress

- `functions.php` へ機能を集約し続ける
- Core API を使わず独自処理を増やす
- `$wpdb` で直接操作し、抽象化を迂回する
- nonce / capability チェックを省略する

## Frontend

- `div` のみで文書構造を作る
- 役割のない ARIA を乱用する
- 小さな挙動へ過剰な JS 依存を持ち込む

## 設計

- 抽象化コストが利益を上回る設計
- 命名が責務を示さない構造
- 修正箇所が複数層に分散する構成
