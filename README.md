# Hitsuki46 ZMK — DYA Studio 対応版

元リポジトリ: [yoshikina17/zmk-config-hitsuki46](https://github.com/yoshikina17/zmk-config-hitsuki46)  
参考: [cormoran/zmk-keyboard-dya2](https://github.com/cormoran/zmk-keyboard-dya2) (v2.0 / main+dya)

## 変更点

- ZMK を **cormoran `main+dya`** に変更
- DYA Studio 用モジュール一式を追加
- PMW3610 を **cormoran studio-rpc 対応ドライバ** に変更
- デュアルトラックボール・NiMH バッテリー・マトリクスは元のまま

## ビルド

GitHub Actions が push で自動ビルドします。  
Artifacts から `hitsuki46_R.uf2` / `hitsuki46_L.uf2` をダウンロードしてフラッシュしてください。

## DYA Studio

https://studio.dya.cormoran.works/

初回は USB 接続 + `studio-rpc-usb-uart` スニペット付きファームで接続できます。

## 注意

- 初回ビルドは west モジュール取得で時間がかかります
- トラックボールの invert / CPI は Studio から調整可能
- LED (WS2812) は基本点灯のみ（元の gohanda widget は一旦外しています）
