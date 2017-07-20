# Videos (v2)

## Get All Videos

```shell
curl "https://www.codeschool.com/api/v2/videos.json"
  -H "Authorization: OAuth thisisyouroauthtoken"
```

> The above command returns JSON structured like this:

```json
{
  "videos": [
    {
      "id": 36,
      "embed_id": "ff2e847",
      "projector_video": {
        "embed_id": "ff2e847",
        "projectable_id": 36,
        "projectable_type": "Video"
      },
      "show_id": 1,
      "path_id": 5,
      "title": "Intro to MVC",
      "position": 132,
      "assets": {
        "path_icon_url": {
          "1x": "https://www.codeschool.com/assets/paths/icon-electives@1x.png",
          "2x": "https://www.codeschool.com/assets/paths/icon-electives@2x.png",
          "3x": "https://www.codeschool.com/assets/paths/icon-electives@3x.png"
        }
      },
      "created_at": "2012-06-14T08:39:05Z",
      "updated_at": "2015-05-07T17:13:02Z"
    },
    {
      "id": 39,
      "embed_id": "5af62185",
      "projector_video": {
        "embed_id": "5af62185",
        "projectable_id": 39,
        "projectable_type": "Video"
      },
      "show_id": 1,
      "path_id": 35,
      "title": "Feature Branches & Pull Requests",
      "position": 129,
      "assets": {
        "path_icon_url": {
          "1x": "https://www.codeschool.com/assets/paths/icon-git@1x.png",
          "2x": "https://www.codeschool.com/assets/paths/icon-git@2x.png",
          "3x": "https://www.codeschool.com/assets/paths/icon-git@3x.png"
        }
      },
      "created_at": "2012-08-08T23:14:02Z",
      "updated_at": "2015-05-07T17:11:58Z"
    },
  ]
}
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
curl "https://www.codeschool.com/api/v2/videos/36.json"
  -H "Authorization: OAuth thisisyouroauthtoken"
```

> The above command returns JSON structured like this:

```json
{
  "videos": {
    "embed_id": "ff2e847",
    "name": "Intro to MVC",
    "files": [
      {
        "url": "http://projector.codeschool.com/videos/ff2e847.mp4?profile=720p&site=codeschool&sso=5uwiJp_5_XFLGiK46VNlNyrKpzqk8iIkmogdTTP4McOwLUrPLGTpZ8T7pA3M5II3wPdAlLDjRH8MHQfQw-GvqZpSsb_Pb8GbNNHfzqo2hHyOk_Gr1Llar7_HXCzjySTA",
        "quality": "hd",
        "type": "video/mp4"
      },
      {
        "url": "http://projector.codeschool.com/videos/ff2e847.mp4?profile=480p&site=codeschool&sso=5uwiJp_5_XFLGiK46VNlNyrKpzqk8iIkmogdTTP4McOwLUrPLGTpZ8T7pA3M5II3wPdAlLDjRH8MHQfQw-GvqZpSsb_Pb8GbNNHfzqo2hHyOk_Gr1Llar7_HXCzjySTA",
        "quality": null,
        "type": "video/mp4"
      },
      {
        "url": "http://projector.codeschool.com/videos/ff2e847.webm?profile=WebM&site=codeschool&sso=5uwiJp_5_XFLGiK46VNlNyrKpzqk8iIkmogdTTP4McOwLUrPLGTpZ8T7pA3M5II3wPdAlLDjRH8MHQfQw-GvqZpSsb_Pb8GbNNHfzqo2hHyOk_Gr1Llar7_HXCzjySTA",
        "quality": null,
        "type": "video/webm"
      }
    ]
  }
}
```

This endpoint returns information about a single video from our screencasts
(Code TV, Feature Focus, and Soup to Bits)

### HTTP Request

`GET https://www.codeschool.com/api/v2/videos/<video_id>.json`

### Query Parameters

None
