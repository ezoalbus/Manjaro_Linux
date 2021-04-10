# Python 3.6 3.7のインストール

## Pythonバージョン
- インストール: `yay -S python36`
- インストール: `yay -S python37`

これらは、`/usr/bin`に格納されている

## poetry
- インストール: `sudo pacman -S python-poetry`
- 使用法: 
  - `poetry init` で初期化
    - ここで、指定したPythonバージョンが存在すれば、勝手に探してくれる   
  - `poetry install` でパッケージをインストール
    - 今後、よくつかうパッケージをまとめたい
    - poetryにも`requirements.txt` に書き出す機能がある
     
