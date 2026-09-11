# サーバーありがとう（周年タワー）

## 編集するのは data.js だけ
- `people` の3つ目にXのID（@なし）を入れると、タップでそのアカウントに飛ぶ
- 空欄の人はタップしても何も起きない
- `official.x` はXのID、または投稿のURLをそのまま入れられる（1口の正方形の並びで空き枠が出たときだけ表示）
- `people` の3つ目も同じく、IDでも投稿URLでも可

## Cloudflare Pages（GitHub連携）
1. このフォルダの中身（index.html / data.js / README.md）を GitHub の `vocabuki-io/Tower` に置く（`main` ブランチ）
2. Cloudflare → Workers & Pages → 作成 → Pages → Gitに接続 → そのリポジトリを選ぶ
3. ビルド設定：フレームワーク「なし」、ビルドコマンド「空欄」、出力ディレクトリ「/」
4. 保存してデプロイ → `プロジェクト名.pages.dev` で公開
5. 以後は GitHub で data.js を編集して保存するたびに自動で反映
