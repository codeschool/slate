# User Courses (v2)

## Get All User::Courses for a User

```shell
curl "https://www.codeschool.com/api/v2/users/<user_id>/courses.json
  -H "Authorization: OAuth poopoopoo
```

> The above command returns JSON structured like this:

```json
{
  "user_courses": [
    {
      "course_id": 158,
      "progress": "100.0"
    },
    {
      "course_id": 24,
      "progress": "0.0"
    },
    {
      "course_id": 15,
      "progress": "100.0"
    }
  ]
}
```

This endpoint returns information about user progress.

### HTTP Request

`GET https://www.codeschool.com/api/v2/users/<user_id>/courses.json`

### Query Parameters

| Parameter | Default | Description                                                        |
|-----------|---------|--------------------------------------------------------------------|
| completed | false   | If true, only courses that the user has completed will be returned |
