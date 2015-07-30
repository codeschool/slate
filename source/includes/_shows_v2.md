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
        "hero_image": "https://www.codeschool.com/assets/shows/brand-soup-to-bits-d9906658736cb6e0aa3cdc14a8448634.svg",
        "hero_background_color": null,
        "videos": [
          {
            "id": 997,
            "show_id": 4,
            "path_id": 5,
            "path_title": "Electives",
            "title": "Soup to Bits: The Sequel to SQL",
            "position": 0,
            "assets": {
              "path_icon_url": {
                "1x": "https://www.codeschool.com/assets/paths/icon-electives@1x.png",
                "2x": "https://www.codeschool.com/assets/paths/icon-electives@2x.png",
                "3x": "https://www.codeschool.com/assets/paths/icon-electives@3x.png"
              }
            }
          },
        ]
      }
    ]
  }
]
```

This endpoint retrieves all Shows.

### HTTP Request

`GET https://www.codeschool.com/api/v2/shows`

### Query Parameters

None

## Get a Show

```shell
curl "https://www.codeschool.com/api/v1/show/4.json"
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
[
  {
    "shows":
      {
        "id": 4,
        "title": "Soup to Bits",
        "description": "View practical steps for building applications following a Code School course. ",
        "short_description": "View practical steps for building applications following a Code School course. ",
        "brand_image": "https://www.codeschool.com/assets/shows/brand-soup-to-bits-d9906658736cb6e0aa3cdc14a8448634.svg",
        "title_image": "https://www.codeschool.com/assets/shows/brand-soup-to-bits-d9906658736cb6e0aa3cdc14a8448634.svg",
        "hero_background_color": "278998",
        "number_videos": 13
      }
  }
]
```

This endpoint retrieves a single Show.

### HTTP Request

`GET https://www.codeschool.com/api/v1/shows/4`

### Query Parameters

none
