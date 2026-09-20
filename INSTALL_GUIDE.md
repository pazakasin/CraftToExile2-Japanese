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
2. 使いたいバージョン用のZIPファイルをダウンロード
   - 例: `CrafttoExile2-JP-for-modpack-v2.1.4.zip`

### ステップ2: ファイルの解凍

1. ダウンロードしたZIPファイルを右クリック
2. 「すべて展開」または「解凍」を選択
3. 適当な場所に解凍（デスクトップなど）
解凍したフォルダ内に以下のフォルダがあることを確認:
```
kubejs/
resourcepacks/
```

### ステップ3: ファイルのコピー

解凍したフォルダを、Minecraftインスタンスフォルダにコピー
```
解凍したフォルダ   → Minecraftインスタンスフォルダ
├── kubejs/         → .instances/Craft to Exile 2/kubejs/
└── resourcepacks/  → .instances/Craft to Exile 2/resourcepacks/
```

最終的に以下のようになります
```
instances/
└ Craft to Exile 2/
    ├─ kubejs/
    │   └─ assets/
    │       └─ ftbquestlocalizer/
    │           └─ lang/
    │               └── ja_jp.json     ← KubeJS管理MOD翻訳ファイル
    └─ resourcepacks/
         └─ MyJPpack/
             ├ pack.mcmeta                ← リソースパック管理ファイル
             └─ assets/
                 └─ <mod_id>/
                     └─ lang/
                         └── ja_jp.json ← リソースパック管理MOD翻訳ファイル
```

### ステップ4: MOD「The Twilight Forest」用の追加設定（任意）

<details>
<summary>クリックして詳細を表示（実施しなくてもプレイ可能です）</summary>

MOD「The Twilight Forest」に同梱されている日本語ファイルに不具合があり、そのファイルが残っていると、MOD「The Twilight Forest」が正しく日本語化されない現象が確認されています。
これを解消するには、MOD本体（jarファイル）の中にある日本語ファイルを削除する必要があります。

1. 7-Zipなど、zipファイルを開けるソフトを用意する（未インストールの場合は[7-Zip公式サイト](https://7-zip.opensource.jp/)などからダウンロード）
2. Minecraftインスタンスフォルダ内の `mods` フォルダを開く
```
   instances/Craft to Exile 2/mods/
```
3. `twilightforest-` から始まるjarファイル（例: `twilightforest-1.20.1-4.3.2508-universal.jar`）を右クリックし、「7-Zipで開く」などを選択
4. jarファイル内を以下の順にたどる
```
   assets/
   └ twilightforest/
       └ lang/
           └ ja_jp.json
```
5. `ja_jp.json` を右クリックし、「削除」を選択
6. 確認画面が出た場合は「はい」を選択し、jarファイルを閉じる

削除が完了すると、MOD「The Twilight Forest」も正しく日本語化されるようになります。

> **注意:** この修正はMOD本体のファイルを直接書き換えるものです。Modpackを更新してMODファイルが再ダウンロード・上書きされた場合、この手順は再度やり直す必要があります。
なお本手順で削除するのは日本語ファイルのみで、MOD自体の機能には影響しません。

</details>

### ステップ5: マイクラの言語設定を日本語に変更

（既に設定済みの場合は不要）

1. Minecraftを起動
2. タイトル画面で「Options」（設定）を開く
3. 「Language」（言語設定）を選択
4. 「日本語（日本）」を選択
4. 「DONE」（完了）を選択

### ステップ6: リソースパックの有効化

1. Minecraftを起動
2. タイトル画面で「設定」を開く
3. 「リソースパック」を選択
4. 左側の「利用可能」リストに「MyJPpack」があることを確認
5. 「MyJPpack」をクリックして右側の「選択中」に移動
6. 「完了」をクリック

### ステップ7: ゲームの再起動

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

日本語化ファイルの新しいバージョンがリリースされたら:

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
