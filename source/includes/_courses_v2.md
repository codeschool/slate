# Courses (v2)

## Get All Courses

```shell
curl "https://www.codeschool.com/api/v2/courses.json"
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
{
  "courses": [
    {
      "id": 9,
      "path_id": 3,
      "state": "available",
      "title": "CSS Cross-Country",
      "position": 42,
      "short_description": "Master the fundamentals and core foundations of CSS.",
      "long_description": "Learn the fundamentals & foundational elements of CSS with CSS Cross-Country. Review all the web-styling necessities for front-end efficiency.",
      "videos_count": 8,
      "level_ids": [
        22,
        23,
        24,
        25,
        26,
        27,
        28,
        29
      ],
      "levels": [
        {
          "id": 22,
          "title": "Frost-Proof Fundamentals",
          "description": "Adding style, selectors, the cascade, and floats",
          "badge_image_url": "https://d1ffx7ull4987f.cloudfront.net/images/achievements/large_badge/41/level-1-on-css-cross-country-96fb99da28e17edb7da62911777bf1d3.png",
          "videos_count": 1,
          "projector_videos": [
            {
              "embed_id": "78e9c182",
              "accessible": false,
              "name": null,
              "position": 1
            }
          ]
        },
      ],
      "has_level_videos": true,
      "assets": {
        "hero": {
          "small": "https://d1ffx7ull4987f.cloudfront.net/images/courses/hero_thumb/9/css-cross-country-05a95971ef5437c4b14f8465a8d67881.jpg",
          "large": "https://d1ffx7ull4987f.cloudfront.net/images/courses/hero/9/css-cross-country-780e5b2658971457c56cca36d28ed61b.png",
          "theme": "light",
          "background_color": "c4e3f3"
        },
        "badge": {
          "small": "https://d1ffx7ull4987f.cloudfront.net/images/achievements/small_badge/40/completed-css-cross-country-4c128be261bb4fd465c8cbfa07178272.png",
          "large": "https://d1ffx7ull4987f.cloudfront.net/images/achievements/large_badge/40/completed-css-cross-country-ec9a9aa14797031680577e7a986bef75.png"
        }
      }
    }
  ]
}
```

This endpoint retrieves all Courses.

### HTTP Request

`GET https://www.codeschool.com/api/v2/courses`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
fake_release | false | If set to true, the result will include a fake release from yesterday and bust the cache. This is useful to test your interface for the event of a course release.

## Get Single Course

```shell
curl "https://www.codeschool.com/api/v2/courses.json"
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
{
  "courses": {
    "id": 104,
    "levels": [
      {
        "id": 206,
        "title": "Forest of Function Expressions",
        "description": "Learn how to use and manipulate functions as expressions.",
        "projector_videos": [
          {
            "embed_id": "15e218c3",
            "files": [
              {
                "url": "http://projector.codeschool.com/videos/15e218c3.mp4?profile=720p&site=codeschool&sso=3ebuCw-5u8SBqa3vPIhrVR7U33Cf3537E7BUKFKD9-Sy5IfGLQh_-ERTE1joWond4q3cvjfbTSHUsLQ0Z04UaW3EqBsYTwQsjT7Qnq_j2mv9RWBi76vrXzwB7VTI86CO",
                "quality": "hd",
                "type": "video/mp4"
              },
            ]
          }
        ]
      }
    ]
  }
}
```

This endpoint retrieves a single Course.

### HTTP Request

`GET https://www.codeschool.com/api/v2/courses/<course id>.json`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
n/a

## Level Videos

```shell
curl "https://www.codeschool.com/api/v2/courses/27/level_videos?level_number=4"
  -H "Authorization: OAuth poopoopoo
```

> The above command returns JSON structured like this:

```json
{
  "courses": [
    {
      "embed_id": "d3f42067",
      "accessible": true,
      "name": null,
      "position": 1,
      "files": [
        {
          "url": "http://projector.codeschool.com/videos/d3f42067.mp4?profile=720p&site=codeschool&sso=n3Oo5Gid5JKxCeY3dRXzBfDbRcjyqanjhVUEFuek89YVkxLXvz-AB5IDkzJmX1Qg03EG5Q58xNI3ZWKq0aGV68iPlRJKWztLWT2TwHmu4-doR5WirXkYgIu3_6UJmCJI",
          "quality": "hd",
          "type": "video/mp4"
        },
        {
          "url": "http://projector.codeschool.com/videos/d3f42067.mp4?profile=480p&site=codeschool&sso=n3Oo5Gid5JKxCeY3dRXzBfDbRcjyqanjhVUEFuek89YVkxLXvz-AB5IDkzJmX1Qg03EG5Q58xNI3ZWKq0aGV68iPlRJKWztLWT2TwHmu4-doR5WirXkYgIu3_6UJmCJI",
          "quality": null,
          "type": "video/mp4"
        },
        {
          "url": "http://projector.codeschool.com/videos/d3f42067.webm?profile=WebM&site=codeschool&sso=n3Oo5Gid5JKxCeY3dRXzBfDbRcjyqanjhVUEFuek89YVkxLXvz-AB5IDkzJmX1Qg03EG5Q58xNI3ZWKq0aGV68iPlRJKWztLWT2TwHmu4-doR5WirXkYgIu3_6UJmCJI",
          "quality": null,
          "type": "video/webm"
        }
      ]
    },
  ]
}
```

This endpoint retrieves information about the videos in a Course Level.

### HTTP Request

`GET https://www.codeschool.com/api/v2/courses/27/level_videos?level_number=4`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
level_number (required) | none | Specifies the level for which information is requested.
