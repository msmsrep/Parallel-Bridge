---
title: Parallel-Bridge-LocalLink ユーザーガイド
seo_title: UNC パス・共有フォルダのリンクをブラウザーから開く (Edge / Chrome)
tagline: 社内サイトに書かれた共有フォルダのパスを、クリックひとつでエクスプローラーに開く
description: Edge や Chrome では開けない社内サイトの共有フォルダのパス (UNC パス・file:// リンク) を、クリックひとつでエクスプローラーに開く無料の Windows アプリと拡張機能。通信は社内で完結し、ログや解析もありません。
lang: ja
locale: ja_JP
alternate: /en/
image: /assets/img/og-ja.png
store_links: true
---

[English]({{ '/en/' | relative_url }}) ・ [プライバシーポリシー]({{ '/privacy-policy' | relative_url }})

社内のグループウェアや Wiki に `\\fileserver\共有\資料.xlsx` のようなパスが書いてあっても、
ブラウザはセキュリティ上の理由でそれを開けません。
**Parallel-Bridge-LocalLink** は、そのパスをクリックひとつでエクスプローラーに開けるようにします。

<figure class="shot">
  <img src="{{ '/assets/img/guide/ja/page-links.png' | relative_url }}" alt="社内ページの共有パスがリンクに変わった様子" loading="lazy">
  <figcaption>有効にしたサイトでは、共有パスがリンクになります</figcaption>
</figure>

- 通信はすべてあなたのパソコンと社内のファイルサーバーの間だけで完結します。
- 開いたフォルダの履歴やログは残しません。広告・アクセス解析・テレメトリもありません。
  → [プライバシーポリシー]({{ '/privacy-policy' | relative_url }})

## 必要なもの

| 項目 | 条件 |
|---|---|
| OS | Windows 10 バージョン 2004 以降、または Windows 11 (64 ビット) |
| ブラウザ | Microsoft Edge または Google Chrome |
| 構成 | Windows アプリ **Parallel-Bridge-LocalLink** と、お使いのブラウザー用の拡張機能 (Edge なら **Parallel-Bridge for Edge**、Chrome なら **Parallel-Bridge for Chrome**) |

アプリだけでも `pbridge://` のリンクは開けますが、
ふつうの社内ページで使うには拡張機能も必要です。

## 1. インストールする

ページ上部のボタン、または下のリンクから、アプリと拡張機能をインストールします。
拡張機能は、お使いのブラウザーに合わせてどちらか一方を入れてください (中身は同じです)。

### Windows アプリ

Microsoft Store から [Parallel-Bridge-LocalLink](https://apps.microsoft.com/detail/9MZS24SFBKR9) をインストールします。

インストールすると、Windows が `pbridge://` リンクをこのアプリに結び付けます。
特別な設定は要りません。

### Edge 拡張機能

Edge アドオンストアから [Parallel-Bridge for Edge](https://microsoftedge.microsoft.com/addons/detail/parallelbridge-for-edge/dmidfkmnkkedmhecpoamhlfmdjacciob) を追加します。

### Chrome 拡張機能

Chrome ウェブストアから [Parallel-Bridge for Chrome](https://chromewebstore.google.com/detail/jkpdfjipibgfpeehjgmcjpahmpfipkfl) を追加します。

Chrome で拡張機能を追加したあとは、ツールバーのパズルのアイコンからピン留めしておくと、
次の手順でアイコンを見つけやすくなります。

## 2. 使いたいサイトで有効にする

拡張機能は、**既定ではどのサイトでも動きません**。
あなたが許可したサイトでだけページを読みます。

1. 共有フォルダのパスが書かれた社内ページを開く
2. ツールバーの「Parallel-Bridge for Edge」(Chrome では「Parallel-Bridge for Chrome」) アイコンをクリック
3. **「このサイトで有効にする」** を押す
4. ブラウザーが「このサイトへのアクセスを許可しますか」と聞くので許可する

<figure class="shot">
  <img src="{{ '/assets/img/guide/ja/popup-enable.png' | relative_url }}" alt="ツールバーのアイコンから「このサイトで有効にする」を押す画面" loading="lazy">
</figure>

これで、そのサイトのパスがリンクに変わります。
やめたいときは同じアイコンから「このサイトで無効にする」を押します。

## 3. リンクをクリックする

リンクをクリックすると、次の順で進みます。

1. **ブラウザーの確認** — 「Parallel-Bridge-LocalLink を開きますか？」という Edge / Chrome の確認が出ます。
   「常に許可」はサイト単位で効きます（別のサイトでは改めて確認が出ます）。
2. **Parallel-Bridge-LocalLink の確認** — 開こうとしている**パスの全文**と、
   リンクが名乗っている送信元が表示されます。内容を確かめて「開く」を押してください。
3. エクスプローラーが開き、対象のファイルが選択された状態になります。

<figure class="shot">
  <img src="{{ '/assets/img/guide/ja/app-confirm.png' | relative_url }}" alt="リンクをクリックすると、開くパスの全文を示す確認画面が出る" loading="lazy">
  <figcaption>Parallel-Bridge-LocalLink の確認画面</figcaption>
</figure>

同じ共有 (`\\サーバー\共有` 単位) をこれから何度も使うなら、
確認画面の **「この共有を常に許可」** を押すと次回から確認が省かれます。

### クリックの使い分け

| 操作 | 動作 |
|---|---|
| クリック | フォルダを開いて対象を選択（推奨） |
| Shift + クリック | 既定のアプリで開く |
| Ctrl + クリック | パスをコピーするだけ |

既定の動作は拡張機能のオプション「クリックしたときの動作」で変えられます。

<figure class="shot">
  <img src="{{ '/assets/img/guide/ja/click-action.png' | relative_url }}" alt="拡張機能のオプション「クリックしたときの動作」" loading="lazy">
</figure>

## 4. 設定

### 拡張機能のオプション

ツールバーのアイコン →「オプションを開く」。

<figure class="shot">
  <img src="{{ '/assets/img/guide/ja/ext-options.png' | relative_url }}" alt="拡張機能のオプション画面" loading="lazy">
</figure>

| 項目 | 説明 |
|---|---|
| 有効にしたサイト | 許可済みサイトの一覧。ここから取り消せます |
| 本文中のパスもリンクにする | リンクになっていない `\\サーバー\共有` という文字列もリンクにします（既定はオフ）。空白を含むパスは `「」` や `" "` で囲まれていれば認識します |
| クリックしたときの動作 | 上の表のとおり |
| 変換したリンクに印を付ける | 変換済みのリンクが見分けられるようになります |

<figure class="shot">
  <img src="{{ '/assets/img/guide/ja/auto-link.png' | relative_url }}" alt="「本文中のパスもリンクにする」のオフとオンで、文章中のパスがリンクになるかどうかを比べた画面" loading="lazy">
  <figcaption>「本文中のパスもリンクにする」をオンにすると、文章中に書かれたパスもリンクになります</figcaption>
</figure>

### アプリの設定

スタートメニューから Parallel-Bridge-LocalLink を起動すると設定画面が開きます。

| 項目 | 説明 |
|---|---|
| 確認なしで開ける共有 | 「この共有を常に許可」を押した共有の一覧。選んで削除できます |
| 動作テスト | UNC パスを入力して、開けるかどうかをその場で確かめられます |
| 言語 | 日本語 / 英語 / Windows の設定に合わせる（次の起動から反映） |
| 設定フォルダを開く | 設定ファイルの保存先を開きます |

<figure class="shot">
  <img src="{{ '/assets/img/guide/ja/app-settings.png' | relative_url }}" alt="アプリの設定画面 (確認なしで開ける共有と言語)" loading="lazy">
</figure>

<figure class="shot">
  <img src="{{ '/assets/img/guide/ja/app-test.png' | relative_url }}" alt="アプリの設定画面の動作テスト" loading="lazy">
  <figcaption>「動作テスト」で UNC パスが受理されるか確かめられます</figcaption>
</figure>

## 5. 困ったとき

### リンクをクリックしても何も起きない

- Windows アプリがインストールされているか確認してください
  (スタートメニューに Parallel-Bridge-LocalLink があるかどうかで分かります)。
- ブラウザーの確認ダイアログを以前「ブロック」してしまった可能性があります。
  アドレスバー左のアイコンからサイトの権限を見直してください。

### そのページのパスがリンクにならない

- そのサイトで「このサイトで有効にする」を押しているか確認してください。
- パスが `<a>` リンクになっていない文章中の文字列の場合は、
  オプションの「本文中のパスもリンクにする」をオンにしてください。
- 有効にしたあとにページを開いていた場合は、ページを再読み込みしてください。

### 「このサーバーは許可リストにありません」と出る

安全のため、Parallel-Bridge-LocalLink は**社内ネットワーク (LAN) 内のサーバー**にしかアクセスしません。
インターネット上のサーバーを指すリンクは開けません。

<figure class="shot">
  <img src="{{ '/assets/img/guide/ja/app-blocked.png' | relative_url }}" alt="「実行ファイルは直接開きません」「このリンクは開けません」の画面" loading="lazy">
</figure>

### 「このパスは見つかりませんでした」「サーバーに接続できませんでした」と出る

パスの綴りを確認してください。
VPN にこれから接続する場合や、オフラインで使えるファイルの場合は
「そのまま開く」で続行できます。

### 「実行ファイルは直接開きません」と出る

`.exe` や `.bat` などの実行ファイルは、安全のため直接は開きません。
代わりに、それが入っているフォルダを表示します。

### 毎回ブラウザの確認ダイアログが出る

Edge / Chrome の仕様です。「常に許可」は**サイト単位**で効くので、
別のサイトからクリックすると改めて確認が出ます。

## 開発を支援する

Parallel-Bridge は無料で使えます。気に入っていただけたら、開発の支援をお願いします。
支援は任意で、使える機能は変わりません。

- [GitHub Sponsors](https://github.com/sponsors/msmsrep)
- [Ko-fi](https://ko-fi.com/msmsrep)

## お問い合わせ

<small>不具合の報告や要望は [GitHub の Issues](https://github.com/msmsrep/Parallel-Bridge/issues) まで。</small>
