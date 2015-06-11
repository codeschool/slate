# Shows (v2)

## Get All Shows

```shell
curl "https://www.codeschool.com/api/v2/shows.json"
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
[
  {
    "shows": [
      {
        "id": 4,
        "title": "Soup to Bits",
        "description": "View practical steps for building applications following a Code School course. ",
        "short_description": "View practical steps for building applications following a Code School course. ",
        "brand_image": "https://www.codeschool.com/assets/shows/brand-soup-to-bits-d9906658736cb6e0aa3cdc14a8448634.svg",
        "title_image": "https://www.codeschool.com/assets/shows/brand-soup-to-bits-d9906658736cb6e0aa3cdc14a8448634.svg",
        "hero_background_color": "278998",
        "number_videos": 13
      },
      {...},
    ]
  }
]
```

This endpoint retrieves all Shows.

### HTTP Request

`GET https://www.codeschool.com/api/v2/paths`

### Query Parameters

None
