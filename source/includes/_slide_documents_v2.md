# Slide Documents (v2)

## Get Slides for Course

```shell
curl "https://www.codeschool.com/api/v2/courses/8/slide_documents.json
  -H "Authorization: OAuth poopoopoo"
```

> The above command returns JSON structured like this:

```json
{
  "slide_documents": [
    {
      "id": 250,
      "name": null,
      "remote_id": "coffeescript.pdf",
      "course_id": 8,
      "remote_url": "http://projector.codeschool.com/documents/coffeescript.pdf?site=codeschool&sso=1OFN7JAlW7Tkm6vGXORwtDdFsB_s474J39AnKgxe3kz1uxQPkQlIGaCES20jj6h8GfdnUZiQUD3ZOF2cMvLm04u8s36MYrGAo32WCYuHg_cvNhgwCnX4nbpUl65yYWYV_VPsF1tGFEplHznHbI_iFA="
    }
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
