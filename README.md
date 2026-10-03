# Luminous Oath（ルミナス・オース）

ブラウザで遊べる3DオープンワールドRPGです。ビルドは不要で、`index.html` 1ファイルだけで動きます（3D描画ライブラリ three.js とフォントはCDNから読み込みます）。

- 第1章「光の大陸アストラリア」／第2章「黄昏の大陸ノクティス」
- 4人パーティ。操作キャラは切り替え可能（Q キー／パーティ欄クリック）
- PC（キーボード・マウス）とスマホ（タッチ操作）の両方に対応
- メニューの「ヘルプ」から、レベルや装備を自由に強化できます

## 遊び方（ローカル）

`index.html` をブラウザで開くだけで遊べます。

## GitHub Pages で公開する

ビルド不要の単一HTMLなので、ブランチの root からそのまま配信できます。

1. このブランチを `main` にマージする
2. リポジトリの **Settings → Pages** を開く
3. **Build and deployment → Source** を「Deploy from a branch」にする
4. **Branch** を `main`、フォルダを `/ (root)` にして **Save**
5. 1〜2分後、次のURLで公開されます

   `https://nakanaka0318.github.io/Arcana-Gunslinger/`

`.nojekyll` を置いているので、Jekyllによる変換はかかりません。

### 新しいリポジトリ `luminous-oath` で公開したい場合

GitHub CLI（gh）を入れたPCで、このリポジトリのフォルダから実行します。

```sh
gh repo create luminous-oath --public --source=. --remote=pages
git push pages HEAD:main
gh api -X POST repos/{owner}/luminous-oath/pages -f "source[branch]=main" -f "source[path]=/"
```

公開URL：`https://<あなたのユーザー名>.github.io/luminous-oath/`
