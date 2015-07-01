# Videos (v2)

## Get All Videos

```shell
curl "https://www.codeschool.com/api/v2/videos.json"
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
{
  "videos": [
      {
        "id": 134,
        "embed_id": "1e18edea",
        "projector_video": {
          "embed_id": "1e18edea",
          "projectable_id": 134,
          "projectable_type": "Video"
        },
        "show_id": 1,
        "path_id": 1,
        "title": "Pearson: Rails Tutorial - Part 1",
        "position": 99,
        "assets": {
          "path_icon_url": {
            "1x": "https://www.codeschool.com/assets/paths/icon-ruby@1x.png",
            "2x": "https://www.codeschool.com/assets/paths/icon-ruby@2x.png",
            "3x": "https://www.codeschool.com/assets/paths/icon-ruby@3x.png"
          }
        },
        "created_at": "2013-07-05T16:53:23Z",
        "updated_at": "2015-05-07T16:58:06Z"
      },
      {...}
}
]
```

This endpoint returns information about videos from our screencasts (Code Tv,
Feature Focus, and Soup to Bits)  URLs are not returned in this endpoint, use
the single video endpoint to obtain them. This endpoint does not return course
videos. Those can be obtained using `/api/v2/courses`

### HTTP Request

`GET https://www.codeschool.com/api/v2/videos`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
show_id   | none    | Return only videos from the show (Code TV, Soup to Bits, Feature Focus) with this ID.

## Get a Video

```shell
curl "https://www.codeschool.com/api/v2/videos.json"
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
{
  "videos": [
    {
      "id": 134,
      "show_id": 1,
      "path_id": 1,
      "title": "Pearson: Rails Tutorial - Part 1",
      "position": 99,
      "assets": {
        "path_icon_url": {
          "1x": "https://www.codeschool.com/assets/paths/icon-ruby@1x-cb0f0911e7bc96edf284b1463d175653.png",
          "2x": "https://www.codeschool.com/assets/paths/icon-ruby@2x-b0644d07fa345aebdf9e2a05c7234e60.png",
          "3x": "https://www.codeschool.com/assets/paths/icon-ruby@3x-5bffc4b95f92105a1d6c589310b7108f.png"
        },
        "files": [
          {
            "url": "http://projector.codeschool.com/videos/1e18edea.mp4?profile=720p&site=codeschool&sso=-pxoRRI-8pozhk1hBVlhNrRVvmK_1ftYcZBRHmtCSW3qeWCkEvRhZf7P3jWYOmZPSRVxeoYhvDCYELBcz3vDHJedOnVAHxL4h3HWH_RQFs9Pw_SVjJy_oJJXbjWafLJA",
            "quality": "hd",
            "type": "video/mp4"
          },
          ...
}
```

This endpoint returns information about a single video from our screencasts
(Code TV, Feature Focus, and Soup to Bits)

### HTTP Request

`GET https://www.codeschool.com/api/v2/videos/<video_id>`

### Query Parameters

None
