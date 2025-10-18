# Signage Maker

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HosoyaYusaku/signage-maker/blob/main/notebooks/signage_maker.ipynb)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Google Colab/Jupyter–based **digital signage HTML generator** with an ipywidgets UI.  
Two rendering modes are available: **Plain (GSAP)** and **Pixi (particle morphing)**.  
It outputs a **single, standalone HTML** page with Wake Lock, fullscreen toggle, and CDN fallback hints.

-----

## ✨ Features

- **Single-file output (standalone HTML)**
  - No build steps. Download and open in a browser.
- **Two modes**
  - **Plain (GSAP)**: Lightweight & stable. Photos and texts loop independently with simple transitions.
  - **Pixi (Particles)**: Photo/text morphing into particles with smooth dot-based animation.
- **Digital-signage friendly**
  - Wake Lock (prevent sleep), key controls (Space/F/R), fullscreen toggle, and reduced-motion awareness.
- **CDN-pinned libraries**
  - **GSAP 3.12.5** via cdnjs with **SRI**.
  - **PixiJS 7.3.3** via cdnjs (SRI optional; functionally unaffected).
- **Image optimization (optional)**
  - Uses Pillow when available to convert/resize to WebP.

-----

## 🚀 Quick Start (Google Colab / Jupyter)

1. Open the notebook: `notebooks/signage_maker.ipynb`.
2. Run the single cell to launch the ipywidgets UI.
3. **Step 1**:  
   - Upload photos (optional; optimization toggle available).  
   - Enter messages in **1b. 表示する文言** (one line = one message).  
     - You can prefix a line with `seconds|text` (e.g., `5|Sale now`) to set per-message duration.
4. **Step 2**:  
   - Build your playback order: add messages/images and adjust the list (move up/down, delete).
5. **Step 3**:  
   - Choose **Plain** or **Pixi** and tweak style/animation parameters.
6. **Step 4**:  
   - Click **「HTMLを生成してダウンロード」** to get either:
     - `signage_plain.html` (Plain/GSAP), or
     - `signage_pixi.html` (Pixi/particles).

**Controls at runtime:**  
- `Space` = Play/Pause, `F` = Fullscreen, `R` = Reload (start from beginning)

> Notes  
> - Wake Lock API may require user interaction and depends on browser/platform.  
> - When `prefers-reduced-motion: reduce` is set, animations slow down for accessibility.

-----

## 🌐 Live Demo (GitHub Pages)

**Project site:** https://hosoyayusaku.github.io/signage-maker/

This page serves as a minimal demo entrypoint for the project (CDN/GSAP/PixiJS/Wake Lock/fullscreen sanity check).

-----

## 🧩 Third-Party

- **GSAP**: https://gsap.com/licensing/  
- **PixiJS**: https://github.com/pixijs/pixijs/blob/main/LICENSE

Additional license details are collected in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

-----

## 📄 License

This project is licensed under the **MIT License**.  
See [LICENSE](LICENSE) for details.

-----

-----

# サイネージメーカー (Signage Maker)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HosoyaYusaku/signage-maker/blob/main/notebooks/signage_maker.ipynb)

Google Colab/Jupyter 上で動く **デジタルサイネージ用 HTML 生成ツール**です。  
ipywidgets ベースの UI を持ち、**Plain（GSAP）** と **Pixi（粒子モーフィング）** の 2 モードを選べます。  
**スタンドアロン HTML** を出力し、Wake Lock・フルスクリーン・CDN フォールバックなどを備えています。

-----

## ✨ 主な機能

- **単一 HTML 出力**
  - ビルド不要。ダウンロードしてブラウザで開くだけ。
- **2つのモード**
  - **Plain（GSAP）**：軽量・安定。写真とテキストを個別ループ＋簡易トランジション。
  - **Pixi（粒子）**：写真や文字を粒子（ドット）で表現し、滑らかに変形。
- **サイネージ向け最適化**
  - Wake Lock（スリープ防止）、キーボード操作（Space/F/R）、フルスクリーン、低モーション配慮。
- **CDN 固定**
  - **GSAP 3.12.5**（cdnjs + SRI）  
  - **PixiJS 7.3.3**（cdnjs／SRIは任意）
- **画像軽量化（任意）**
  - Pillow がある環境では WebP 変換・縮小に対応。

-----

## 🚀 使い方（Colab / Jupyter）

1. `notebooks/signage_maker.ipynb` を開く  
2. 単一セルを実行して UI を起動  
3. **Step 1**  
   - 写真をアップロード（任意・軽量化ON可）  
   - **1b. 表示する文言** に1行1メッセージで入力  
     - 行の先頭に `秒数|テキスト`（例: `5|ただいまセール中`）と書けば、その行だけ秒数指定
4. **Step 2**  
   - 順序リストに追加して、上/下/削除で並べ替え
5. **Step 3**  
   - **Plain** または **Pixi** を選択して細かい見た目や動きを調整
6. **Step 4**  
   - **「HTMLを生成してダウンロード」** を押して以下のいずれかを取得  
     - `signage_plain.html`（Plain/GSAP）  
     - `signage_pixi.html`（Pixi/粒子）

**再生時の操作**  
- `Space` = 再生/一時停止、`F` = 全画面、`R` = リロード（先頭から）

> 補足  
> - Wake Lock はブラウザや端末に依存します（ユーザー操作が必要な場合あり）。  
> - `prefers-reduced-motion: reduce` 設定時はアニメーションがややスロウになります。

-----

## 🌐 デモ（GitHub Pages）

**公開URL:** https://hosoyayusaku.github.io/signage-maker/

本リポジトリの最小デモ用エントリです（CDN/GSAP/PixiJS/Wake Lock/フルスクリーンの疎通確認）。

-----

## 🧩 サードパーティ

- **GSAP**: https://gsap.com/licensing/  
- **PixiJS**: https://github.com/pixijs/pixijs/blob/main/LICENSE

詳細は [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) に集約しています。

-----

## 📄 ライセンス

このプロジェクトは **MIT ライセンス** で公開されています。  
詳しくは [LICENSE](LICENSE) をご覧ください。
