# Paths (v2)

## Get All Paths

```shell
curl "https://www.codeschool.com/api/v2/paths.json"
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
[
  {
    "paths": [
      {
        "id": 1,
        "name": "Ruby",
        "description": "Master your Ruby skills and increase your Rails street cred by learning to build dynamic, sustainable applications for the web.",
        "course_ids": [
          6,
          18,
          5,
          28,
          101,
          108,
          10,
          2,
          14,
          20,
          22,
          1
        ],
        "slug": "ruby",
        "assets": {
          "badge_urls": {
            "svg": "https://www.codeschool.com/assets/paths/badge-ruby-a3ca50c1c68afbe5c766b36835a181d9.svg",
            "png": "https://www.codeschool.com/assets/paths/badge-ruby-59f7ecf395012b45e90e927d5e337786.png"
          },
          "icon_url": {
            "1x": "https://www.codeschool.com/assets/paths/icon-ruby@1x-cb0f0911e7bc96edf284b1463d175653.png",
            "2x": "https://www.codeschool.com/assets/paths/icon-ruby@2x-b0644d07fa345aebdf9e2a05c7234e60.png",
            "3x": "https://www.codeschool.com/assets/paths/icon-ruby@3x-5bffc4b95f92105a1d6c589310b7108f.png"
          },
          "header_image": "https://d1ffx7ull4987f.cloudfront.net/images/paths/path_header/1/ruby-7d985ff0d7aade31a476c746938736d4.png",
          "background_color": "#b24626"
        },
        "path_subgroups": [
          {
            "subpath": {
              "title": "Getting Started With Ruby on Rails",
              "description": "Ruby is an expressive, dynamic programming language. Ruby on Rails is an open source web framework for building custom web applications.  The courses in this section get you quickly up to speed with the basics of the Ruby language and on track to building your first Rails application.",
              "id": 1,
              "path_id": 1,
              "path_position": 1,
              "course_ids": [
                6,
                18,
                5
              ]
            }
          },
        ]
      }
    ]
  }
]
```

This endpoint retrieves all Paths.

### HTTP Request

`GET https://www.codeschool.com/api/v2/paths`

### Query Parameters

None.

<aside class="notice">
The Path endpoint doesn't return nested course data. You'll need to query the Courses endpoint using the course IDs
that each Path returned.
</aside>
