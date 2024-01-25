---
marp: true
---

<!--
theme: gaia
class:
 - invert
headingDivider: 2
paginate: true
-->

<!--
_class:
 - lead
 - invert
-->

# Deno で爆速定期実行

Deno Cron で定期実行のバーゲンセール

## 自己紹介（Twitter: @taroosg）

```json
{
  "name": "Taro Ohsugi",
  "works": [
    {
      "work": "🎓 G's ACADEMY FUKUOKA 主任講師",
      "skills": ["JavaScript", "React", "PHP", "Laravel"]
    },
    {
      "work": "🎓 エンジニア",
      "skills": ["Laravel", "JavaScript", "画面設計", "DB設計"]
    }
  ],
  "like": ["💻", "📚", "🛩️ 🚌 🚅 🚃", "🥃 🍷 🍺", "🚮"]
}
```

# 定期実行したくないですか？？

<!--
_class:
 - lead
 - invert
-->

## 定期実行したいとき

- バックアップ

- メール送信

- データの取得

- etc...

## 定期実行するときの課題

- サーバを用意する（お金がかかる）

- 何が実行されているかの管理が面倒．

- 重複実行されると詰む．

## そこで Deno Cron

<!-- 左右中央に画像を表示 -->

![w:840 drop-shadow bg](./img/deno-cron.png)

## いつもの Deno

![w:340 drop-shadow bg](./img/Deno_2021.svg)

## Deno とは

- Node.js の作者が作った新しい JavaScript/TypeScript の実行環境．

- 標準で TypeScript が使える．

- Deno 公式が様々な機能を提供している．

JS や TS に慣れている人ならすぐに使える．

## Deno のいろいろな機能

Web 開発で使用する機能が標準で提供されている．個人開発くらいなら全部無料．

- Deno Deploy（ホスティング環境）

- Fresh Framework（web アプリケーションのフレームワーク）

- Deno KV（key-value ストレージ）

- 🆕 Deno Cron（定期実行）

## Deno Cron の特徴

- コードが楽．

- 実行内容やログが確認しやすい．

- 重複実行されない．

- お金がかからない．

## コード

```ts
Deno.cron("Sample cron", "*/1 * * * *", () => {
  console.log("Every minute, Deno Deploy runs this without a server");
});
```

以上だ！

## デモ

定期実行が簡単にできるので，自作の API にリクエストを送ってみる．

## 良さげな点

- 実装 → デプロイが爆速．

- デフォルトで重複実行されない．

- 管理画面が良き．

- お金がかからない．

# 🥃

<!--
_class:
 - lead
 - invert
-->

### Enjoy!
