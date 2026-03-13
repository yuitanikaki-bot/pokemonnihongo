# ポケモン にほんご — セットアップ手順

## ファイル構成
```
pokemon-pwa/
├── index.html      ← メインアプリ
├── manifest.json   ← PWA設定
├── sw.js           ← オフライン対応
├── icon-192.png    ← アイコン（小）
├── icon-512.png    ← アイコン（大）
└── README.md       ← この説明書
```

---

## 📦 Step 1: GitHub にアップロード

1. https://github.com にアクセスしてアカウント作成（無料）
2. 「New repository」で新しいリポジトリを作成
   - 名前例: `pokemon-nihongo`
   - **Public** に設定
3. このフォルダの5ファイルをすべてアップロード

---

## 🌐 Step 2: GitHub Pages を有効にする

1. リポジトリの「Settings」→「Pages」
2. Source を「Deploy from a branch」
3. Branch を「main」、フォルダを「/ (root)」に設定
4. 保存すると数分でURLが発行される
   例: `https://あなたのユーザー名.github.io/pokemon-nihongo/`

---

## 📱 Step 3: iPadのホーム画面に追加

1. iPad の Safari で上記URLを開く
2. 画面下部の共有ボタン（□↑）をタップ
3. 「ホーム画面に追加」をタップ
4. 名前「ポケにほん」のまま「追加」
5. ホーム画面にアイコンが現れる → タップするとアプリとして起動！

---

## ✈️ オフライン（機内）での使い方

- 一度Wi-Fiがある場所でアプリを開いておくと、次回以降はオフラインでも動きます
- ポケモンの画像はWi-Fiのある時だけ表示されます（オフライン時は空白）
- テキスト・ひらがな・カタカナ・書き方ガイドはオフラインでも使えます

---

## 🐾 ポケモンを増やしたい場合

`index.html` の `POKEMON` 配列に以下の形式で追加するだけ：

```javascript
{ en:"pikachu", jp:"ピカチュウ", hira:"ぴかちゅう", romaji:"Pi-ka-chu", syl:["Pi","ka","chu"], id:25 },
```

- `id` = 図鑑番号（pokeapi.co で確認できます）
- 追加後、ファイルをGitHubに再アップロードするだけで自動反映されます
