# FNF-friskEngine-beta

TXT ファイルだけで動く、シンプルな FNF 風リズムゲームエンジンです。  
譜面・音声・背景・メタ情報をすべてテキストで管理し、`mods/` フォルダに置くだけで MOD として読み込めます。

---

## 特徴

- ブラウザだけで動作（HTML + JS のみ）
- `mods/フォルダ名/` を追加するだけで MOD を増やせる
- 譜面は `chart.txt`、音声は `audio.txt`（Base64）、背景は `bg.txt`（Base64）
- `meta.txt` でタイトル・作者・難易度・説明文などを定義
- `select.html` から MOD を選択して起動

---

## ファイル構成

```text
FNF-friskEngine-beta/
├─ index.html              # エンジン本体（?mod=xxx で起動）
├─ select.html             # MOD選択画面
├─ README.md               # このファイル
│
├─ mods/
│   ├─ list.json           # MOD一覧（select.html が読む）
│   │
│   └─ testmod/            # サンプルMOD
│        ├─ chart.txt      # 譜面データ
│        ├─ audio.txt      # 音声データ（Base64）
│        ├─ bg.txt         # 背景画像（Base64）
│        ├─ thumb.png      # サムネイル（任意）
│        └─ meta.txt       # MOD情報
│
└─ assets/                 # 追加素材（任意）
