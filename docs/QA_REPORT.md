# NicoGura 公開・確認レポート

確認日: 2026-10-04

## 公開結果

| 項目 | 結果 |
| --- | --- |
| 公開URL | <https://mochidukiakiya.github.io/nicogura-rules/> |
| 専用リポジトリ | <https://github.com/mochidukiakiya/nicogura-rules> |
| 構成 | HTML / CSS / Vanilla JavaScript、GitHub Pages |
| 外部の実行時ライブラリ | 0 |
| データの管理元 | `data/rules.json` |
| ページ | HOME / RULES / CHANGELOG / 編集画面 / 専用404 |
| 正式公開ルール | 0件 |
| 掲載準備の案内カード | 18件 |
| 仮カテゴリー | 18件 |
| 公開前チェック | PASS・公開対象20ファイル |
| 既存ゲームリポジトリへの本作業の変更 | 0件 |

公開中のカードは掲載準備の案内です。運営承認を確認できた正式本文はなく、他サーバーの本文や一般的なFiveMルールを公式ルールとして追加していません。

## 実ブラウザでの機能確認

| 確認内容 | 結果 |
| --- | --- |
| 全文検索 | PASS・「メカニック」で1件に絞り込み、一致語を強調表示 |
| 表記の正規化 | PASS・全角「ＰＤ」で1件に絞り込み、一致語を強調表示 |
| カテゴリー絞り込み | PASS |
| カードの全展開・全閉鎖 | PASS |
| ブックマーク | PASS・再読み込み後も保存状態を維持 |
| ルールのリンクコピー | PASS・対象の個別URLと一致 |
| 個別URL | PASS・検索語、カテゴリー、保存済みフィルターがある状態からも絞り込みを解除して対象を展開 |
| リンク先の画面位置 | PASS・カテゴリーと個別カードを固定ヘッダーの下に表示 |
| ダーク・ライト | PASS・切り替えと選択の保存を確認 |
| モバイルメニュー | PASS・開閉とEscapeキーによる閉鎖を確認 |
| 変更履歴 | PASS・掲載した履歴を表示 |
| 編集フォームの入力保持 | PASS・未適用の入力を同じカードの再選択で失わない |
| 編集内容のダウンロード | PASS・実際にダウンロードしたJSONでタイトルと未適用のサイトバージョンを確認 |
| 未追加カテゴリーの扱い | PASS・未追加の入力がある間は書き出しを中断 |
| 専用404 | PASS・プロジェクトURL配下の深い未知パスでも表示 |

正常な公開ページでのJavaScriptコンソールエラーは0件でした。確認した既知リンク8件はHTTP 200で応答しました。未確定の外部URLは設定を空欄にしており、リンクを表示していません。

独立した静的監査で内部参照101件・61種類のURLを確認し、欠落ファイル・欠落IDは0件でした。このリンク切れ件数は確認した内部URLの範囲です。

## 画面サイズ

HOMEとRULESを次のサイズで確認し、全サイズで文書の幅が画面幅を超えないことを確認しました。

| 確認サイズ | 結果 |
| --- | --- |
| モバイル幅320px | PASS |
| モバイル幅375px | PASS |
| モバイル幅390px | PASS |
| モバイル幅430px | PASS |
| 768 × 1024px | PASS |
| 1366 × 768px | PASS |
| 1440 × 900px | PASS |
| 1920 × 1080px | PASS |

## 大量データ・長文の確認

公開しないローカルの検証用データで120件のルールを読み込みました。3353文字の長文、重要カード20件の自動展開、「人質」で120件に一致する検索と強調表示を確認しました。検証時の処理時間は実行環境で約292msでした。これは測定環境での目安です。

検証用の本文は公開データには含まれていません。公開データは正式0件・案内18件のままです。

## 静的検査・公開前監査

- 5ページのHTML検証: PASS
- JavaScriptの構文検査: PASS
- JSONの構造、ID・番号の重複、カテゴリー・注目ルール参照、日付、画像の存在: PASS
- 危険なスクリプト・URL、認証情報、内部IP・パスらしい文字列の検査: PASS
- 検証用の異常JSONを拒否する動作: PASS
- 静的サーバーの公開範囲、未知パスの404、隠しファイル・パス移動の拒否: PASS
- 公開成果物を許可したファイルだけに限定するGitHub Actions: PASS

既存ゲームリポジトリの変更状態を作業前後で比較し、本作業による変更がないことを確認しました。

## Lighthouse実測

| 測定対象 | Performance | Accessibility | Best Practices | SEO |
| --- | ---: | ---: | ---: | ---: |
| 公開RULES | 99 | 100 | 100 | 100 |
| 公開HOME | 98 | 100 | 100 | 100 |

公開RULESのCLSは0、LCPは1.3秒、公開HOMEのCLSは0、LCPは1.9秒でした。スコアは検証時の環境・データでの実測値です。端末、回線、キャッシュ、コンテンツ更新によって変動し、常時同じスコアを保証するものではありません。

## デザインと参考資料

NicoGuraの既存ロゴ、ヘッダー、アイコンを使用しました。夜色を基調に、パステルのピンク・青と控えめなガラス表現を組み合わせ、色・余白・角丸をCSS変数で管理しています。

[情報整理の参考サイト](https://yurugura.notion.site/316d3a104c9180aeb2d8fb09f7ed8a22)と[ClownRPのルールサイト](https://clownrp.com/rules/)は実ブラウザで確認しました。カテゴリー、番号、見出し、スマートフォンでの読みやすさを検討の参考にし、文章・画像・CSSをコピーしていません。

## 運営確認が必要な内容

次の18カテゴリーは仮の分類で、正式本文はすべて運営確認中です。

基本ルール、RPルール、禁止事項、市民、公務員、PD、EMS、メカニック、店舗 / Business、犯罪、Heist、ギャング、武器、車両、配信 / SNS、運営対応、罰則、FAQ。

本文の掲載条件と引き継ぎ事項は [CONTENT_STATUS.md](CONTENT_STATUS.md) にまとめています。正式な本文を承認後、`data/rules.json` の該当カードを更新し、`status` を `published` にしてください。Discord、X、FiveM、外部公式URLも確認済みのURLだけを設定します。

## 更新と今後の拡張

ブラウザ編集画面は <https://mochidukiakiya.github.io/nicogura-rules/editor/> です。編集内容をダウンロードし、運営確認後にGitHubの `data/rules.json` を置き換えてCommitします。この画面には認証・サーバー保存・直接公開の機能はありません。詳細な更新方法は [README](../README.md) に記載しています。

ブランド画像の差し替え対象は、`assets/logo.webp`、`city.webp`、`icon.webp`、`og.png`、`favicon.png`、`apple-touch-icon.png` です。公式リンクは `site.links`、本文・カテゴリー・更新履歴は `data/rules.json` で管理します。

GUIDE、JOBS、CITY、FAQ、NEWS等は、運営承認済みの内容ができてから追加できます。正式本文が増えた段階で、実際のルール数と本文量による検索・目次・表示性能を再確認してください。

## ディレクトリ概略

```text
nicogura-rules/
├── index.html                 HOME
├── rules/index.html           RULES
├── changelog/index.html       CHANGELOG
├── editor/index.html          ブラウザ編集画面
├── 404.html                   専用404
├── assets/                    ブランド画像・CSS・JavaScript
│   ├── app.js                 公開サイトの機能
│   ├── style.css              デザイン
│   ├── editor.js              JSONのブラウザ編集
│   └── data-validation.js     共通データ検証
├── data/rules.json            本文・カテゴリー・サイト設定
├── scripts/
│   ├── serve.mjs              ローカル確認
│   └── validate.mjs           公開前監査
├── docs/                      掲載状況・確認レポート
├── .github/workflows/pages.yml 公開ワークフロー
├── robots.txt
├── sitemap.xml
└── README.md                  運営向け更新手順
```

GitHub Pagesの公開成果物にはREADME、docs、開発用スクリプトを含めません。公開リポジトリにはゲームの設定・認証情報・内部資料・個人情報を追加しません。
