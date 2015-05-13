# Courses (v2)

## Get All Courses

```shell
curl "https://www.codeschool.com/api/v2/courses.json"
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 7,
    "path_id": 2,
    "state": "available",
    "title": "jQuery Air: Captain's Log",
    "position": 23,
    "short_description": "Introduce yourself to the most useful jQuery techniques. Soon to be discontinued.",
    "long_description": "Learn jQuery best practices & useful techniques of jQuery's efficient JavaScript library. Let jQuery Air: Captain's Log help you make the most of your code.",
    "videos_count": 4,
    "level_ids": [
      124,
      125,
      126,
      127
    ],
    "has_level_videos": false,
    "credits": "- **Gregg Pollack** *Professors*\r\n- **Eric Allam** *Content Contributors*\r\n- **Drew Barontini** *Designers*\r\n- **Drew Barontini** *Front-end Development*\r\n- **Eric Allam** *Challenge Implementation*\r\n- **Less Films** *Video Production*",
    "assets": {
      "hero": {
        "small": "https://www.codeschool.com/images/courses/hero_thumb/7/jquery-air-captains-log-6a86bb1fcc843912dd59e96b418a89b9.jpg",
        "large": "https://www.codeschool.com/images/courses/hero/7/jquery-air-captains-log-e7bdc37d16e57bb717bb5a8df238a490.jpg",
        "theme": "light",
        "background_color": "EFE3D0"
      },
      "badge": {
        "small": "https://www.codeschool.com/images/achievements/small_badge/30/completed-jquery-air-captain-s-log-4c74a49096cad0262e4e5a5b30c7cb7f.png",
        "large": "https://www.codeschool.com/images/achievements/large_badge/30/completed-jquery-air-captain-s-log-0f4b90723003d3c9c132ed6270298be5.png"
      }
    }
  },
]
```

This endpoint retrieves all Courses.

### HTTP Request

`GET https://www.codeschool.com/api/v2/courses`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
fake_release | false | If set to true, the result will include a fake release from yesterday and bust the cache. This is useful to test your interface for the event of a course release.


## Level Videos

```shell
curl "https://www.codeschool.com/api/v2/courses/27/level_videos?level_number=4"
  -H "Authorization: OAuth poopoopoo
```

> The above command returns JSON structured like this:

```json
[
  {
    "embed_id": "b69e8dcb",
    "accessible": true,
    "name": "A Video",
    "position": 1,
    "files": [
      {
        "url": "http://projector.dev/videos/b69e8dcb.mp4?profile=720p&site=codeschool&sso=3p-gFOslNuF6GLD2QS7IF-S0RVSqdQCD5RJ3lM93g0LFQBQfKqpI8FDjIqFAF_BUFB9-i-m_qNO3770adF2CXImzTuWEMYfXcdQ6vI9mNoStC3isYzuNL12uuA5TT6P-",
        "quality": "hd",
        "type": "video/mp4"
      },
      {
        "url": "http://projector.dev/videos/b69e8dcb.mp4?profile=480p&site=codeschool&sso=3p-gFOslNuF6GLD2QS7IF-S0RVSqdQCD5RJ3lM93g0LFQBQfKqpI8FDjIqFAF_BUFB9-i-m_qNO3770adF2CXImzTuWEMYfXcdQ6vI9mNoStC3isYzuNL12uuA5TT6P-",
        "quality": null,
        "type": "video/mp4"
      },
      {
        "url": "http://projector.dev/videos/b69e8dcb.webm?profile=WebM&site=codeschool&sso=3p-gFOslNuF6GLD2QS7IF-S0RVSqdQCD5RJ3lM93g0LFQBQfKqpI8FDjIqFAF_BUFB9-i-m_qNO3770adF2CXImzTuWEMYfXcdQ6vI9mNoStC3isYzuNL12uuA5TT6P-",
        "quality": null,
        "type": "video/webm"
      }
    ]
  },
  {
    "embed_id": "a9804880",
    "accessible": true,
    "name": "A Video",
    "position": 2,
    "files": [
      {
        "url": "http://projector.dev/videos/a9804880.mp4?profile=720p&site=codeschool&sso=goxLfxIRXixROwCGldFNuPcIftE8ibL8PGLd7o8UnMoua3he4djEq15_JynOGn86_v11pYXtYKZ6xd5OrcSFwoeF61IbXYRgW2tZ_rk-bKABJEJ624CO70c28_EP92XX",
        "quality": "hd",
        "type": "video/mp4"
      },
      {
        "url": "http://projector.dev/videos/a9804880.mp4?profile=480p&site=codeschool&sso=goxLfxIRXixROwCGldFNuPcIftE8ibL8PGLd7o8UnMoua3he4djEq15_JynOGn86_v11pYXtYKZ6xd5OrcSFwoeF61IbXYRgW2tZ_rk-bKABJEJ624CO70c28_EP92XX",
        "quality": null,
        "type": "video/mp4"
      },
      {
        "url": "http://projector.dev/videos/a9804880.webm?profile=WebM&site=codeschool&sso=goxLfxIRXixROwCGldFNuPcIftE8ibL8PGLd7o8UnMoua3he4djEq15_JynOGn86_v11pYXtYKZ6xd5OrcSFwoeF61IbXYRgW2tZ_rk-bKABJEJ624CO70c28_EP92XX",
        "quality": null,
        "type": "video/webm"
      }
    ]
  },
  {
    "embed_id": "5fe62c1e",
    "accessible": true,
    "name": "A Video",
    "position": 3,
    "files": [
      {
        "url": "http://projector.dev/videos/5fe62c1e.mp4?profile=720p&site=codeschool&sso=8HEr0Zl7ATdit3miXhzAtIQt5R1bLQ6NUlP9kpfqt-K9MjfSmoF6aKF0UEXDPFJlX6XhuBguVN872zsZapkUoIqiPGQyfkCEc5MAdhPFL_T_w47UqI0bXVl8ZCdKk4VO",
        "quality": "hd",
        "type": "video/mp4"
      },
      {
        "url": "http://projector.dev/videos/5fe62c1e.mp4?profile=480p&site=codeschool&sso=8HEr0Zl7ATdit3miXhzAtIQt5R1bLQ6NUlP9kpfqt-K9MjfSmoF6aKF0UEXDPFJlX6XhuBguVN872zsZapkUoIqiPGQyfkCEc5MAdhPFL_T_w47UqI0bXVl8ZCdKk4VO",
        "quality": null,
        "type": "video/mp4"
      },
      {
        "url": "http://projector.dev/videos/5fe62c1e.webm?profile=WebM&site=codeschool&sso=8HEr0Zl7ATdit3miXhzAtIQt5R1bLQ6NUlP9kpfqt-K9MjfSmoF6aKF0UEXDPFJlX6XhuBguVN872zsZapkUoIqiPGQyfkCEc5MAdhPFL_T_w47UqI0bXVl8ZCdKk4VO",
        "quality": null,
        "type": "video/webm"
      }
    ]
  }
]
```

This endpoint retrieves information about the videos in a Course Level.

### HTTP Request

`GET https://www.codeschool.com/api/v2/courses/27/level_videos?level_number=4`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
level_number | none | Specifies the level for which information is requested.
position | none | Specifies, by position, the video within the level for which information is requested
