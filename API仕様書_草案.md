# API仕様書（草案）
## 1. 飯屋検索API

```GET /restaurants```

### パラメータ
|   命名   | データ型 |         説明        |
|----------|--------|--------------------|
| category |string[]|カテゴリ（複数設定可能）|
| latitude | number |     緯度            |
| longitude| number |     経度            |

#### クエリ例
```https://api.cocomeshi.com/restaurants?category[]=xxx&category[]=yyy&longitude=135.12345&latitude=42.12345```


### レスポンス

```json
{
    "hit_num": 100,
    "restaurants": [
        {
            "id": 12345,
            "name": "マクドナルド",
            "homepage_url": "",
            "address": "",
            "opentime_start": "",
            "opentime_close": "",
            "categories": ["喫茶店", "ジャンクフード"],
            "image_url_list": ["", "", ""],
            "latitude": 42.53769,
            "longitude": 135.12345
        },
        ...
    ]
}

```

<br>

## 2. カテゴリ一覧API

```GET /categories```

### パラメータ
なし

#### クエリ
```https://api.cocomeshi.com/categories```

### レスポンス

```json
{
    "categories": []
}
```

