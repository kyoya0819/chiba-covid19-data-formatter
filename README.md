# chiba-covid19-data-format

使いづらかったので作りました。

## 必要なもの

- [ここ](https://www.city.chiba.jp/hokenfukushi/iryoeisei/seisaku/covid-19/opendata.html) から「千葉市患者発生発表数」をダウンロード（2021/08/24基準で作ってます）
- Composer（基本バージョンはなんでも動くはず）
- PHP（8以上。ただ、7.4でも動作に問題はないはず）

## 使い方

```
$ composer install
$ php artisan 入力ファイル名 出力形式 出力ファイル名
```

- 出力形式は`csv`か`json`

## サンプル

```
$ php artisan data.xlsx json data.json
$ php artisan data.xlsx csv data.csv
```

## 出力形式

### json

```json
{
    "日付": "感染者数",
    ...
}
```

### csv

```csv
date,number
日付,感染者数
...
```

## ライセンス

このソースコードはMITライセンスです。

## その他

1時間ぐらいで作ったのでissue / PRお待ちしています！！