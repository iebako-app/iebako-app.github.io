# iebako-app.github.io

イエバコ（家庭在庫管理 iOS アプリ）の公式サイト。GitHub Pages で配信される静的サイト。

## 公開 URL

- ルート: https://iebako-app.github.io/
- ヘルプ: https://iebako-app.github.io/help/
- フィードバック: https://iebako-app.github.io/feedback/
- プライバシーポリシー: https://iebako-app.github.io/privacy/
- 利用規約: https://iebako-app.github.io/terms/

## 構成

```
.
├── index.html              # ランディング
├── assets/
│   ├── style.css           # 共通スタイル（Light/Dark 自動対応）
│   └── icon.png            # アプリアイコン
├── help/index.html         # ヘルプ・FAQ
├── privacy/index.html      # プライバシーポリシー
├── terms/index.html        # 利用規約
└── feedback/index.html     # Google フォームへの導線
```

## 技術構成

- 純粋な静的 HTML + CSS（ビルドステップなし）
- フレームワーク・JS なし
- Apple のシステムフォント（-apple-system / Hiragino Sans）を優先
- `prefers-color-scheme` でダークモード自動対応

## 編集の流れ

1. ローカルで該当 HTML を編集
2. ブラウザでファイルを直接開いて確認、または `python3 -m http.server` でローカルサーバ起動
3. `git add` → `git commit` → `git push origin main`
4. GitHub Pages が数十秒で公開反映

## 改訂が必要なとき

- **プライバシーポリシー / 利用規約**: 内容変更時は `最終更新日` と末尾の `改訂履歴` を必ず更新
- **ヘルプ**: 機能追加・変更時に対応する FAQ エントリを更新
- **アプリアイコン**: アプリ本体側で更新したら `assets/icon.png` も差し替え

## カスタムドメインに切り替えるとき（将来）

1. ドメイン購入（例: iebako.app）
2. このリポジトリのルートに `CNAME` ファイルを置き、中身に `iebako.app` と書く
3. ドメイン側で `iebako-app.github.io` を CNAME / A レコードで指す
4. GitHub リポジトリの Settings → Pages → Custom domain でドメインを設定
5. HTTPS 強制チェックボックスを ON
