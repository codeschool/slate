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
      "id": 2,
      "name": null,
      "remote_id": "assembling_sass_notes.pdf"
    }
  ]
}
```

This endpoint retrieves all SlideDocuments for the given course

### HTTP Request

`GET
https://www.codeschool.com/api/v2/courses/[course_id]/slide_documents.json`

### Query Parameters


