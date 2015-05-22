# Course Slides (v2)

## Get Slides for Course

```shell
curl "https://www.codeschool.com/api/v2/courses/17/slide_documents.json
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
{
  "slide_documents": [
    {
      "course_id": 17,
      "id": 1,
      "name": null,
      "remote_id": "assembling_sass_notes.pdf"
    },
    {
      "course_id": 23,
      "id": 1,
      "name": null,
      "remote_id": "git_real_notes.pdf"
    },
    {...}
  ]
}
```

This endpoint retrieves all SlideDocuments for the given course

To obtain the actual files, make a `GET` request to
`http://www.codeschool.com/documents/<remote_id>`, where `remote_id` is
that returned by the `slide_documents` endpoint.

### HTTP Request

`GET
https://www.codeschool.com/api/v2/courses/[course_id]/slide_documents.json`

### Query Parameters

No parameters accepted
