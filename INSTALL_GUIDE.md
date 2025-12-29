# インストールガイド

Craft to Exile 2 日本語化ファイルのインストール方法を詳しく説明します。

## 📋 事前準備

### 必要なもの

- ✅ Craft to Exile 2がインストール済み
- ✅ Minecraft 1.20.1
- ✅ 日本語化ファイル（本リポジトリから入手）

### Minecraftインスタンスフォルダの場所

ランチャーごとのインスタンスフォルダ:

| ランチャー | デフォルトパス |
|-----------|---------------|
| **CurseForge** | `C:\Users\<ユーザー名>\curseforge\minecraft\Instances\Craft to Exile 2` |
| **FTB App** | `C:\Users\<ユーザー名>\FTBApp\instances\Craft to Exile 2` |
| **MultiMC/Prism** | `<MultiMCフォルダ>\instances\Craft to Exile 2\.minecraft` |
| **AT Launcher** | `C:\Users\<ユーザー名>\ATLauncher\instances\Craft to Exile 2` |

インスタンスフォルダが分からない場合:
1. ランチャーでCraft to Exile 2を右クリック
2. 「フォルダを開く」または「Open Folder」を選択

---

## 🚀 インストール手順

### ステップ1: 日本語化ファイルのダウンロード

1. [Releases](https://github.com/pazakasin/CraftToExile2-Japanese/releases)ページを開く
2. 最新版のZIPファイルをダウンロード
   - 例: `CrafttoExile2-JP-v1.0.0.zip`

### ステップ2: ファイルの解凍

1. ダウンロードしたZIPファイルを右クリック
2. 「すべて展開」または「解凍」を選択
3. 適当な場所に解凍（デスクトップなど）
解凍したフォルダ内に以下のフォルダがあることを確認:
```
config/
resourcepacks/
```

### ステップ3: ファイルのコピー

解凍したフォルダを、Minecraftインスタンスフォルダにコピー
```
解凍したフォルダ   → Minecraftインスタンスフォルダ
├── config/         → .instances/Craft to Exile 2/config/ （※）
└── resourcepacks/  → .instances/Craft to Exile 2/resourcepacks/
  ※：configはファイル差し替えのため、フォルダのバックアップ推奨
```

最終的に以下のようになります
```
instances/
└ Craft to Exile 2/
    ├─ config/
    │   └─ ftbquests/
    │       └─ quests/
    │           └── *.snbt             ← クエスト翻訳ファイル、既存の英語ファイルを差し替え
    └─ resourcepacks/
         └─ MyJPpack/
             ├ pack.mcmeta                ← リソースパック管理ファイル
             └─ assets/
                 └─ <mod_id>/
                     └─ lang/
                         └── ja_jp.json ← リソースパック管理MOD翻訳ファイル
```

### ステップ4: マイクラの言語設定を日本語に変更

（既に設定済みの場合は不要）

1. Minecraftを起動
2. タイトル画面で「Options」（設定）を開く
3. 「Language」（言語設定）を選択
4. 「日本語（日本）」を選択
4. 「DONE」（完了）を選択

### ステップ5: リソースパックの有効化

1. Minecraftを起動
2. タイトル画面で「設定」を開く
3. 「リソースパック」を選択
4. 左側の「利用可能」リストに「MyJPpack」があることを確認
5. 「MyJPpack」をクリックして右側の「選択中」に移動
6. 「完了」をクリック

### ステップ6: ゲームの再起動

1. Minecraftを完全に終了
2. 再度起動

---

## ✅ 確認方法

### クエストが日本語化されているか確認

1. ゲーム内でクエストブック（通常はインベントリに自動追加）を開く
2. クエスト名や説明が日本語になっていればOK

### MODが日本語化されているか確認

1. 適当なMODアイテム（例: Create MODの歯車など）にカーソルを合わせる
2. アイテム名が日本語表示されていればOK

---

## 🔧 トラブルシューティング

### Q1: 一部のMODが日本語にならない

**原因1**: リソースパックが有効化されていない

**解決方法**: 「設定」→「リソースパック」で「MyJPpack」が右側（選択中）にあるか確認

**原因2**: そのMODの翻訳が未対応

**解決方法**: [Issues](https://github.com/pazakasin/CraftToExile2-Japanese/issues)、またはX（旧Twitter）の[@willAtDev](https://x.com/willAtDev)に翻訳リクエストを送ってください

### Q2: ゲームが起動しない

**原因**: ファイルコピー時にゲームファイルを破損した可能性

**解決方法**:
1. 念のため、変更前にバックアップを取っておく
2. バックアップから復元
3. 再度、慎重にファイルをコピー

通常、翻訳ファイルの追加でゲームが起動しなくなることはありません。

### Q3: 英語と日本語が混在する

**原因**: 一部のMODが未翻訳、または機械翻訳ツールの翻訳漏れ

**解決方法**:
- これは正常です
- 完全翻訳は段階的に進めています
- 気になる部分はIssuesで報告してください

---

## 🔄 更新方法

新しいバージョンがリリースされたら:

1. 最新版のZIPをダウンロード
2. 上記の「ステップ2」以降を繰り返す
3. 既存ファイルを上書き（マージ）でOK

---

## 📞 サポート

問題が解決しない場合:
- [Issues](https://github.com/pazakasin/CraftToExile2-Japanese/issues)、またはX（旧Twitter）の[@willAtDev](https://x.com/willAtDev)で質問
- 上記のトラブルシューティングも参照

---

**インストール成功を祈っています！楽しいCraft to Exile 2ライフを！ 🎮**
