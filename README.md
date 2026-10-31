# CoreEngineGames

[CoreEngine](https://github.com/tanahara0310/CoreEngine) で作ったゲームとシーンの置き場です。
エンジンのリポジトリを軽くするため、重いアセットを使うプロジェクトをこちらへ分けました。

## 中身

| フォルダ | 中身 |
|---|---|
| `Projects/Sandbox` | 実在のアラハビーチ（北谷町）のシーン `ArahaBeachScene`、沖縄の海辺 `OkinawaBeachScene`、Shadertoy から移した海 `SeascapeScene` など |
| `Projects/Reprism` | レプリズム。C++ で作ったゲームをスクリプトだけで作り直したパズルアクション |
| `Projects/Tsunagazaru` | つながザルをえない。C++ で作ったゲームをスクリプトだけで作り直したトロッコのゲーム |
| `Tools/OkinawaBeach` | 沖縄とアラハビーチのモデルを Blender で作って書き出すスクリプト |
| `Tools/XBot` | 人型（Mixamo の X Bot）のアニメーションをまとめるスクリプト |
| `CoreEngine` | エンジン（サブモジュール）。このゲームが動くエンジンの版を記録しています |

## 開き方

エンジンのリポジトリを横に並べて置き、エンジンのエディタからプロジェクトを開きます。

```
C:\CoreEngine\        エンジン（ビルドしてエディタを起動する）
C:\CoreEngineGames\   このリポジトリ
```

1. `C:\CoreEngine` でエディタをビルドして起動します。
2. プロジェクトの選択の右上にある **追加…** を押し、`C:\CoreEngineGames\Projects\Sandbox` などのフォルダを選びます。一覧に足されるので、選んで **開く** を押します。2 回目からは一覧から開けます。

エディタで保存したシーンやアセットの変更は、このリポジトリに入ります。エンジンの変更は `C:\CoreEngine` のリポジトリにコミットします。

## エンジンのサブモジュール

`C:\CoreEngine` を使うなら、`CoreEngine` フォルダの中身は取り出さなくて構いません。
別の PC でエンジンごと取り出すときは、最新版だけを取ると軽く済みます。

```bash
git submodule update --init --depth 1 CoreEngine
```

## Tools

スクリプトは、このリポジトリの根から動かします。書き出したモデルは `Projects/Sandbox/Application/Assets/Models` に入ります。

```bash
python Tools/OkinawaBeach/build_araha_town.py
```

使い方は `Tools/OkinawaBeach/README.md` にあります。
