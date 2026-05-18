# SPACE INDEX × ORBIT STORIES

> 日本の宇宙ビジネス参入を、データと物語の両面から支える知識基盤

このリポジトリには、宇宙産業参入を検討する企業・個人向けの2つの独立したサイトが含まれています。

## 🌍 二つのサイト

### 📚 [SPACE INDEX](./index.html) — 体系的なリファレンス

参入を体系的に検討する人のための知識基盤。参入カテゴリの全体像、ビジネスモデル、初期費用、政府支援プログラム、信頼できる情報源──「どの分野に、いくらかけて、どう入るのか」を網羅。

- 21分野の参入カテゴリマップ
- 14分野のビジネスモデルと初期費用
- 53以上の政府支援プログラム（宇宙戦略基金・SBIR・Kプログラム等）
- 88件の情報源ライブラリ（検索・ソート可）
- 5ペルソナ別の参入ステップ

→ **「左脳で参入を計画する」ためのサイト**

### 🛰 [ORBIT STORIES](./stories.html) — 実話で発見するインスピレーション

衛星データを使って既に動いている、22業界・76の実話を集めた事例ギャラリー。「自分の業界でもこんなことができるのか」と気づくための発見の場。

- 11業界グループの "もう動いている" 事例
- ピックアップ10物語（ラグビー日本代表、タクシー需要予測、アマゾン違法伐採検知…）
- 76の物語をフィルタ可能なギャラリーで検索
- 51件の基礎知識・まとめ記事＋45件の実証記事
- 6年間の事例増加タイムライン

→ **「右脳で参入の意欲をかき立てる」ためのサイト**

データソースは [宙畑（Sorabatake）](https://sorabatake.jp/) のインタビュー・解説記事。

## 公開する

### GitHub Pages で公開する場合

1. このリポジトリの **Settings → Pages** を開く
2. **Source** を「Deploy from a branch」、**Branch** を `main`、フォルダを `/ (root)` に設定して保存
3. 数分後、以下のURLでアクセス可能：
   - SPACE INDEX: `https://<username>.github.io/<repository>/`
   - ORBIT STORIES: `https://<username>.github.io/<repository>/stories.html`

### ローカルで確認する場合

```bash
git clone https://github.com/<username>/<repository>.git
cd <repository>
# 任意のブラウザで開くだけ
open index.html         # SPACE INDEX
open stories.html       # ORBIT STORIES

# あるいはローカルサーバーで
python3 -m http.server 8000
# → http://localhost:8000/ (SPACE INDEX)
# → http://localhost:8000/stories.html (ORBIT STORIES)
```

## ファイル構成

```
.
├── index.html         # SPACE INDEX (参入リファレンス, 約120KB)
├── stories.html       # ORBIT STORIES (事例ギャラリー, 約95KB)
├── README.md          # 本ファイル
├── LICENSE            # MIT License
├── CONTRIBUTING.md    # 貢献ガイドライン
└── .gitignore
```

## 編集する

各HTMLファイル内に、すべてのデータが JavaScript 配列として埋め込まれています。

### SPACE INDEX のデータ

`index.html` 内の以下の配列：

| 配列名 | 内容 | 件数 |
|---|---|---|
| `categories` | 参入カテゴリ | 21 |
| `businessModels` | ビジネスモデルと支援プログラム | 14 |
| `pathways` | ペルソナ別参入ステップ | 5 |
| `resources` | 情報源 | 88 |

### ORBIT STORIES のデータ

`stories.html` 内の以下の配列：

| 配列名 | 内容 | 件数 |
|---|---|---|
| `GROUPS` | 業界グループ定義（色・アイコン・タグライン） | 11 |
| `ARTICLES` | インタビュー記事 | 115 |
| `BASICS` | 基礎知識・まとめ記事 | 51 |
| `DEMOS` | 実証・妄想記事 | 45 |

新しい事例を追加するには、対応する配列にオブジェクトを追記します。詳細は [CONTRIBUTING.md](./CONTRIBUTING.md) を参照。

## データソース

- **JAXA 宇宙戦略基金**：[fund.jaxa.jp](https://fund.jaxa.jp/)
- **内閣府 宇宙政策委員会**：[www8.cao.go.jp/space/](https://www8.cao.go.jp/space/)
- **経済産業省 製造産業局 宇宙産業課**
- **宙畑（Sorabatake）**：[sorabatake.jp](https://sorabatake.jp/) — ORBIT STORIES の物語の源泉
- Novaspace, Bryce Tech, 各企業IR等

## 技術仕様

- **形式**：単一HTMLファイル × 2（CSS・JS インライン）
- **依存**：Google Fonts のみ
- **対応ブラウザ**：モダンブラウザ（Chrome / Firefox / Safari / Edge の最新版）
- **レスポンシブ**：スマートフォン・タブレット・PCに対応
- **データ更新**：HTMLファイル内のJS配列を直接編集

## ライセンス

このプロジェクトは [MIT License](LICENSE) のもとで公開されています。

## 貢献

情報の追加・修正提案は Issue または Pull Request でお願いします。詳細は [CONTRIBUTING.md](./CONTRIBUTING.md) を参照。

特に以下の追加情報を歓迎します：

- 新規の政府支援プログラム情報（SPACE INDEX）
- 新しい衛星データ活用事例の記事（ORBIT STORIES）
- 国内外の信頼できる情報源
- 各分野の最新の価格・コスト情報

## 謝辞

- ORBIT STORIES のすべての物語は [宙畑（Sorabatake）](https://sorabatake.jp/) のインタビュー記事に基づきます。日本の宇宙データ業界の最前線を6年以上にわたり丁寧に取材し続けてきた編集チームに敬意を表します。
- 政府支援プログラムや業界統計の情報は、JAXA・内閣府・経産省・各種業界団体の公開資料に基づきます。

---

*次の物語は、あなたから。*
