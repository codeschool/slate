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
  },
  {
    "id": 54,
    "path_id": 1,
    "title": "Delayed Job",
    "position": 2
  },
  {
    "id": 23,
    "path_id": 1,
    "title": "Rails Anatomy",
    "position": 15
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
