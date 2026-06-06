# 英語ボキャブラリー 音声学習プレイヤー

CSVファイルをアップロードして使う英語音声学習アプリです。
外部APIは一切使用しないため、完全無料で動作します。

## CSVフォーマット（5列）

| 列 | 内容 | 例 |
|---|---|---|
| A列 | 発音記号 | /spaʊs/ |
| B列 | 英単語・フレーズ | spouse |
| C列 | 英語例文 | My spouse cooks well. |
| D列 | 単語の日本語訳 | 配偶者 |
| E列 | 例文の日本語訳 | 私の配偶者は料理が上手です。 |

- 1行目はヘッダー行として自動スキップされます
- `#セクション名` の行でセクション分けができます

## デプロイ手順（Vercel）

```bash
# 1. GitHubリポジトリを作成してプッシュ
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/<ユーザー名>/vocab-player.git
git push -u origin main

# 2. vercel.com でリポジトリを選択してDeploy
```

## 機能

- 英語 → 日本語訳 → 英語例文 → 例文の日本語訳 の順で読み上げ
- 読み上げ速度調整（0.6×〜1.4×）
- セクション選択
- シャッフルモード
- 自動で次へ進む / 手動モード
- フラッシュカード表示（タップで反転）
