# Videos (v2)

## Get All Videos

```shell
curl "https://www.codeschool.com/api/v2/courses.json"
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
"videos": [
  {
    "id": 136,
    "path_id": 1,
    "title": "Pearson: Rails Tutorial - Part 2",
    "position": 16
    "files": [
      {
        "url": "http://projector.codeschool.com/videos/e0a1d1ba.mp4?profile=720p&site=codeschool&sso=3YCxuoMkA3r3TYVft226_FyE-3N8E5rbyWgaM6xjzB4y7Evxwh1lY4Rnh0kUtrtoWxtH3XIbjGzn-b3uOQ3NNReeK4MthlxyizeHyOjoUyBJsSPx3E0CBO1XbJyy997i",
        "quality": "hd",
        "type": "video/mp4"
      },
      {...},
    ]
  },
  { ... },
]
```

This endpoint returns information about videos from Code Tv,
Feature Focus, and Soup to Bits (as opposed to information about the
course level videos).

### HTTP Request

`GET https://www.codeschool.com/api/v2/courses`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
show_id   | none    | Return only videos from the show (Code TV, Soup to Bits, Feature Focus) with this ID.
