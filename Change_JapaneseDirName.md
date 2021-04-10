# home配下のディレクトリを英語表記に変更

## 手順

- `xdg-user-dirs-gtk` のインストール

```
sudo pacman -S xdg-user-dirs-gtk
```

- 英語表記のディレクトリを作成

```
LC_ALL=C xdg-user-dirs-gtk-update
```
---
既存の「空でない」日本語表記ディレクトリは消えないので、手動で消す。

## 参考
- https://wiki.archlinux.org/index.php/XDG_user_directories
