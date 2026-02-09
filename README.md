## ステージング
https://www.sho-recruit.jp/stg_shinsotsu/
※Basic認証設定は下記でリネームして設置しております。
pasu__.htaccess
pasu__.htpasswd


## 本番
https://www.sho-recruit.jp/shinsotsu/

# sho-recruit.jp — Production Repository

このリポジトリは **sho-recruit.jp（本番）** 公開用ソースを管理します。

---

## ブランチ運用（重要）
- `main`：**正（本番）ブランチ**
- 修正・追加作業は **必ず `main` からブランチを切って**進めてください

例：
- `feature/xxxx`（機能追加 / 改修）
- `fix/xxxx`（バグ修正）
- `hotfix/xxxx`（緊急修正）

---

## 作業の流れ（推奨）
1. `main` からブランチ作成
2. 変更 → commit → push
3. Pull Request を作成（`feature/*` → `main`）
4. レビュー後に `main` へマージ
5. （必要に応じて）デプロイ / 公開作業を実施

---

## プロジェクト構成
/
├─ assets/
│  ├─ css/   # 生成物（CSSは原則直接編集しない）
│  ├─ img/
│  └─ js/
├─ src/
│  ├─ js/    # JSソース（common.jsの圧縮前はここ）
│  └─ scss/  # SCSSソース（ここを編集）
├─ inc/      # 共通パーツ（ヘッダー/フッター等）
├─ *.html
└─ index.html

---

## コーディングルール（最低限）
- CSSは原則 `src/scss/` を編集し、ビルドして反映してください
- `assets/css/` は生成物のため、原則として直接編集しない運用を推奨します

---

## キービジュアル（THREE.js 関連）
作業のベースは以下です：
- HTML：`inc/hero.html`
- SCSS：`src/scss/layouts/_kv.scss`
- JS（読み込み）：`inc/heroscript.html`
- JS（実装）：`assets/js/hero.js`

新規スクリプトを追加した場合は、`inc/heroscript.html` に読み込みタグを追記してください。

## プルリクエストtest
