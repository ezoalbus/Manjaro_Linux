# Manjaro Linuxインストール手順
## インストールメディアの書き込み(in USB)
- [公式サイト](https://manjaro.org/download/)からXFCE版のisoファイルをダウンロード
- RufusでUSBに書き込み
## インストール
- BIOSのブート順序を変更しUSBを優先させる
- 起動するとブートマネージャー画面が表示されるので、日本語キーボードの設定等をする
  - Driverに関しては、NVidia製のグラボを積んでいるためプロプライエタリを選択した
- デスクトップ画面からインストールを選択（この際、無線LANが認識されていなかったため有線で接続した）
  - もろもろを設定
  - インストール先の設定
    - ストレージデバイスを選択では確実にインストール先を確認（複数ディスクある場合は抜いて一つにすると安心）
    - ディスクの消去を選択
    - password等の設定
## 設定
### 日本語対応
`sudo pacman -S manjaro-asian-input-support-fcitx fcitx-mozc`

参考:https://qiita.com/oioi/items/8835afc5d2db643efeda

### yayのインストール
「ソフトウェアの追加と削除(Pamac)」から`yay`をインストール

### Google Chromeのインストール
`yay -S google-chrome` もしくはGitHubから

### カーネルヘッダーのインストール
- カーネルの確認
  - `$ uname -r`

- リポジトリでヘッダーを検索

```
$ pamac search linux510
5.10.23-1-MANJARO
```

- インストール
  - `$ pamac install linux510-headers`

## コマンド履歴の一部
- 日本語対応
  - `sudo pacman -S manjaro-asian-input-support-fcitx fcitx-mozc kcm-fcitx`
- ホスト名の変更
  - `hostnamectl set-hostname z440`
- Google Chrome
  - `sudo pacman -S base-devel`
  - `git clone https://aur.archlinux.org/google-chrome.git`
  - `cd google-chrome/`
  - `makepkg -sri`
