## c7rpi-builder

## 内容
c7rpi-builder は、CentOS Userland 7 for Raspberry Pi 2/3/4 のカスタムイメージを作成するスクリプトです。

## 要件
- CentOS Userland 7 が稼働している Raspberry Pi 2B / 3B / 3B+ / 4B
    - [SpecialInterestGroup/AltArch/armhfp - CentOS Wiki](https://wiki.centos.org/SpecialInterestGroup/AltArch/armhfp)
    - [公式イメージ](http://isoredirect.centos.org/altarch/7/isos/armhfp)
- root権限
- anaconda、lorax、python-six および依存パッケージがインストールされていること

## 実行例
```
# ./c7rpi-builder kickstarts/c7rpi-ks.cfg
```

## デフォルトからの変更内容
- キーボードと言語を日本語に変更
- タイムゾーンを Asia/Tokyo に変更
- スワップパーティションを削除
- 代わりにスワップファイル管理スクリプトを追加
- cockpit を追加
- yum-utils を追加
- Bluetooth と Wi-Fi を無効化
- history のフォーマットを変更
- EPEL リポジトリを追加
- CR リポジトリを有効化

## イメージ
- [イメージのダウンロード](https://github.com/lunatilia/c7rpi-builder/releases/tag/1.0.2-20191225)

## ライセンス
[GNU General Public License v2.0](https://github.com/lunatilia/c7rpi-builder/blob/master/LICENSE) (The CentOS Projectのデフォルトライセンス)

