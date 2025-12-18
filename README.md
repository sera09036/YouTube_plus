# YYouTube+

YYouTube+ は、`yt-dlp` を使った動画ダウンロードをサポートします。

**Python + Tkinter GUI アプリケーション**です。

シンプルな操作で YouTube をはじめとする様々な動画サイトから  
動画・音声を取得できます。

---

## ライセンスについて
YYouTube+ は [yt-dlp](https://github.com/yt-dlp/yt-dlp?tab=readme-ov-file#installation)  に準じるものとします。

yt-dlp はUnlicense ライセンスで提供されていますが、リリース ファイルの多くには、異なるライセンスを持つ他のプロジェクトのコードが含まれています。

また、PyInstaller にバンドルされた実行可能ファイルには GPLv3+ ライセンスのコードが含まれており、そのため結合された作業はGPLv3+の下でライセンスされていることです。

## ✨ 特徴

- 🖥 **GUI 対応（Tkinter）**  
  コマンド不要で簡単操作が可能。

- 🎬 **yt-dlp を内部で実行**  
  最新の yt-dlp を用いた強力なダウンロード機能。

- 📦 **PyInstaller による単一 EXE 配布（onefile 対応）**

- 🔄 **自動バージョン管理（bumpver）**
  `pyproject.toml` と `version.py` が連動して更新されます。

- ⚙ **Windows で動作確認済み**

---

## 📥 インストール（開発者向け）

### 1. リポジトリをクローン

```bash
git clone git@github.com:sera09036/YouTube_plus.git
cd Youtube-plus
```

### 2. 依存関係のインストール
YYouTube+は yt-dlpに依存する為、下記の動作環境を推奨致します。

- Pythonバージョン3.10以降（その他のバージョンでは動作が不安定になる恐れがあります。）

- [ffmpegとffprobe](https://www.ffmpeg.org/) をダウンロードし、プロジェクトファオルダ内に　/bin　を追加してください。

また、ffmpegにはバグがあり、yt-dlpと併用すると様々な問題を引き起こします。ffmpegは重要な依存関係にあるため、これらの問題の一部を修正したカスタムビルド[yt-dlp/FFmpeg-Builds](https://github.com/yt-dlp/FFmpeg-Builds)の利用を推奨致します。


**重要:** 必要なのは ffmpegバイナリであり、同じ名前の Python パッケージではありません。

- [yt-dlp-ejs](https://github.com/yt-dlp/ejs) YouTubeのn/sig値の解読に必要です

また、[yt-dlp-ejs を実行するには、 deno（推奨）](https://deno.land/)、node.jsなどの　JavaScriptランタイム　が必須になります。


詳しくは [yt-dlpのリポジトリ](https://github.com/yt-dlp/yt-dlp?tab=readme-ov-file#dependencies)からご確認ください。


### 3. 開発環境構築
パッケージのインストールは .venv等の仮想環境で行うことを推奨いたします。
またpython環境仮想化ツールとしてこのプロジェクトでは　uv を用いてます。
[uvの導入方法](https://docs.astral.sh/uv/getting-started/installation/)はこちらからご確認ください。

