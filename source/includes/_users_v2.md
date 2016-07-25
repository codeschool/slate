# Users (v2)

## Get current User

Given a `token` you obtain from using the Authentication endpoint,
you can query the User endpoint in order to obtain data about this user.

```shell
curl "https://www.codeschool.com/api/v1/user"
  -H "Authorization: OAuth token_from_authentication_endpoint"
```
> The above command returns JSON structured like this:

```json
{
  "user": {
    "id": 33,
    "email": "olivier@codeschool.com",
    "twitter_name": "olivierlacan",
    "name": "Olivier Lacan",
    "username": "olivierlacan",
    "total_score": 365250,
    "completed_courses": [
      160,
      8,
      4,
      # etc.
    ],
    "completed_levels_count": 149,
    "watched_screencasts_count": 163,
    "avatar": "http://gravatar.com/avatar/797569464d2fe9387739c169811d2d60.jpg?s=80&r=pg&d=http%3A%2F%2Fgravatar.com%2Favatar%2F1c02274fedcce55a289172bfb8db25ab.jpg%3Fs%3D80%26r%3Dpg",
    "token": "OAKCnKYoWP8amckAxHZ2KitlkRJQpLb0aV6YDHxI",
    "paid_courses_access": true
  }
}
```

This endpoint retrieves the current User.

### HTTP Request

`GET https://www.codeschool.com/api/v1/user`

### Query Parameters

None.

## User Sign Up

```shell
curl "https://www.codeschool.com/api/v1/users"
  -H "Authorization: OAuth poopoopoo"
  -d "user[email]=ada@lovelace.com&[user]password=bernouli"
```
> The above command returns JSON structured like this:

```json
{
  "user": {
    "id": 33,
    "email": "olivier@codeschool.com",
    "twitter_name": "olivierlacan",
    "name": "Olivier Lacan",
    "username": "olivierlacan",
    "total_score": 365250,
    "completed_courses": [
      160,
      8,
      4,
      # etc.
    ],
    "completed_levels_count": 149,
    "watched_screencasts_count": 163,
    "avatar": "http://gravatar.com/avatar/797569464d2fe9387739c169811d2d60.jpg?s=80&r=pg&d=http%3A%2F%2Fgravatar.com%2Favatar%2F1c02274fedcce55a289172bfb8db25ab.jpg%3Fs%3D80%26r%3Dpg",
    "token": "OAKCnKYoWP8amckAxHZ2KitlkRJQpLb0aV6YDHxI",
    "paid_courses_access": true
  }
}
```

This endpoint creates a User and returns it.

### HTTP Request

`POST https://www.codeschool.com/api/v1/users`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
user[email] | Yes | The prospective user's email address.
user[password] | Yes | The requested password (must be longer than 6 characters).
user[username] | No | The requested username (can be already taken).
user[name] | No | The user's full name (first and last).

## Reset Password for a User

Given a `login` which could either be the user's `username` or the
`email` address associated with their account.

```shell
curl "https://www.codeschool.com/api/v1/users/<login>/reset_password"
  -d
  -H "Authorization: OAuth poopoopoo"
```
> The above command doesn't return any body.

This endpoint sends a reset password to a single User.

### HTTP Request

`POST https://www.codeschool.com/api/v1/users/<username>/reset_password`

### Query Parameters

None.
