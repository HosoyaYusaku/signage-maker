# Signage Maker (Google Colab)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A browser-based tool to generate **standalone digital signage HTML** from your images and text messages.  
It offers two rendering modes (Plain / Pixi Particles), fullscreen controls, a wake-lock hint for kiosk-style usage, and reduced-motion awareness.

> **Note**: The generated HTML relies on CDN scripts (version-pinned). A network connection is required at playback time.

-----

## ✨ Features

- **Two Modes**
  - **Plain (CSS/GSAP)**: Lightweight and stable. Images and messages loop independently with smooth transitions.
  - **Pixi Particles**: Advanced effects. Text and images morph into particle forms.
- **Keyboard Controls**
  Space: play/pause · **F**: fullscreen · **R**: restart.
- **Signage-Oriented Details**
  Wake Lock (when supported), first-time fullscreen tip, reduced-motion friendly timings, and a fallback screen when CDN fails.
- **CDN + Version Pinning**
  GSAP `3.12.5` (with SRI) and PixiJS `7.3.3` are pinned for reproducibility.
- **One-File Output**
  Generates `signage_plain.html` or `signage_pixi.html` that can be hosted or opened locally (network needed for CDN).

-----

## 🚀 How to Use (Colab)

1. Open the notebook `notebooks/signage_maker.ipynb` in Google Colab (or Jupyter).
2. Run the cell to render the UI.
3. **Step 1a**: Upload images (optional but recommended).
4. **Step 1b**: Enter messages.  
   - One message per line.  
   - Prefix with seconds like `5|SALE` to show that line for 5 seconds.  
   - The initial sample text is only **“サンプル１”**. It is auto-added **only once** on first run.
5. **Step 2**: Arrange order (add lines/images, move up/down, delete).
6. **Step 3**: Choose mode (Plain / Pixi) and tweak colors/sizes.
7. Click **“HTMLを生成してダウンロード”** to export the file.

-----

## 📋 Message Format

- **Basic**: one line = one message.  
- **Per-line duration**: `X|your message` → display that line for X seconds (float allowed).  
- **Default duration**: if not specified per line, uses the slider value in Step 1b.  
- **Limits**: up to 50 message lines recommended; a single line up to 120 characters recommended.

-----

## 📦 Output

- `signage_plain.html` — Simple slideshow with GSAP-powered transitions (fade/slide), independent loops for images/messages.
- `signage_pixi.html` — Particle morphing transitions using PixiJS.

-----

## 🔒 Licenses

- Project: MIT (see [LICENSE](LICENSE)).
- Third-party licenses: see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

-----

-----

# サイネージメーカー (Google Colab)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

画像とテキストから**単一 HTML ファイル**のデジタルサイネージを生成するツールです。  
通常表示（Plain）／Pixi 粒子演出の 2 モード、フルスクリーン操作、スリープ防止のヒント、reduced-motion 配慮などを備えています。

> **注意**：出力 HTML は CDN のスクリプト（バージョン固定）に依存します。再生時はネットワーク接続が必要です。

-----

## ✨ 主な機能

- **2つの表示モード**
  - **通常（CSS/GSAP）**：軽量・安定。写真とテキストを独立にループ表示。
  - **Pixi 粒子版**：高度な演出。文字や画像を粒子でモーフィング。
- **キーボード操作**
  スペース：再生/一時停止・**F**：全画面・**R**：最初から。
- **サイネージ向けの配慮**
  Wake Lock（対応環境）、初回の全画面ヒント、reduced-motion への配慮、CDN 読み込み失敗時のフォールバック表示。
- **CDN＋バージョン固定**
  GSAP `3.12.5`（SRI 付き）／PixiJS `7.3.3` を固定。
- **単一ファイル出力**
  `signage_plain.html` または `signage_pixi.html` を生成（再生時はネットワークが必要）。

-----

## 🚀 使い方（Colab）

1. `notebooks/signage_maker.ipynb` を Google Colab（または Jupyter）で開きます。
2. セルを実行して UI を表示します。
3. **Step 1a**：写真をアップロード（任意だが推奨）。
4. **Step 1b**：文言を入力。  
   - 1 行につき 1 メッセージ。  
   - `5|セール中` のように先頭に秒数を付けると、その行だけ表示秒数を個別指定できます。  
   - 初期サンプルは **「サンプル１」** のみ。初回のみ自動追加され、それ以降は無視されます。
5. **Step 2**：順序編集（追加・移動・削除）。
6. **Step 3**：モード選択（通常／粒子）と色・サイズ調整。
7. **「HTMLを生成してダウンロード」** をクリックして出力します。

-----

## 📋 メッセージ形式

- **基本**：1 行 = 1 メッセージ  
- **行ごとの秒数**：`秒|テキスト` 形式（小数可）  
- **既定秒数**：行頭に秒数がない場合は Step 1b のスライダー値を使用  
- **推奨上限**：行数 50、1 行の長さ 120 文字程度

-----

## 📦 出力

- `signage_plain.html` — GSAP によるフェード/スライド切替。画像と文言は独立ループ。
- `signage_pixi.html` — PixiJS による粒子モーフィング演出。

-----

## 🔒 ライセンス

- 本プロジェクト：MIT（[LICENSE](LICENSE)）  
- 併用ライブラリのライセンス： [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)
