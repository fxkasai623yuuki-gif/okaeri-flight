# おかえりフライト キット

## すぐに動かす（今夜のうちに）

1. GitHub で新しいリポジトリを作る（例: `okaeri-flight`）。このフォルダの中身をすべて入れて push する。
   - `.claude/settings.json` も入れる（ループ中に git push や Web 読み込みのたびに許可を聞かれて止まらないようにするため）。
2. GitHub の Settings → Pages で、Branch を `main` / `/ (root)` にして保存。1〜2分で `https://<ユーザー名>.github.io/okaeri-flight/` が開けるようになる。
3. このフォルダで `claude` を起動し、`loop-prompt.md` のコマンドを貼る。
4. PC をスリープしない設定にする（到着の2時間後くらいまで）。

⚠️ GitHub Pages は URL を知っていれば誰でも見られます。便名と時刻は載りますが、座席番号や名前は載せていません。

## デザインを作り直す（余裕があれば）

1. `01_ChatGPTへのデザイン依頼.md` を ChatGPT に貼る。
2. 出てきた HTML を `design/chatgpt.html`、方針の文章を `design/chatgpt-notes.md` に保存する。
3. ループとは別の Claude Code セッションで、`02_ClaudeCodeへのデザイン実装依頼.md` を貼る。

## ファイル

- `index.html` … 表示ページ（今のデザイン、`status.json` を1分ごとに読む）
- `status.json` … 運航データ（9/17 19:15 時点の情報を反映済み）
- `CLAUDE.md` … Claude Code 用の説明と、運航データ更新の手順
- `loop-prompt.md` … ループ用のコマンド
- `.claude/settings.json` … ループ用の許可設定
- `01_…` / `02_…` … デザイン作り直し用の依頼文
