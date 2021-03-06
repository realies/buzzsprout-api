Episodes
========
Run the following examples in Postman [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/cb76cd4a27641f4e1a04)

Get episodes
------------

* `GET /episodes.json` will return all the episodes for a podcast.

```json
[

  {
    "id":788881,
    "title":"Too small or too big?",
    "audio_url":"https://www.buzzsprout.com/140447/788881-filename.mp3",
    "artwork_url":"https://storage.buzzsprout.com/variants/NABbMDx7JN5bSLzLPXyj67jA/8d66eb17bb7d02ca4856ab443a78f2148cafbb129f58a3c81282007c6fe24ff2",
    "description":"",
    "summary":"",
    "artist":"Muffin Man",
    "tags":"",
    "published_at":"2019-09-12T03:00:00.000-04:00",
    "duration":12362,
    "hq":true,
    "guid":"Buzzsprout788881",
    "inactive_at":null,
    "episode_number":5,
    "season_number":5,
    "explicit":false,
    "private":false
  },
  {
    "id":788880,
    "title":"Too fast or too slow?",
    "audio_url":"https://www.buzzsprout.com/140447/788880-filename.mp3",
    "artwork_url":"https://storage.buzzsprout.com/variants/NABbMDx7JN5bSLzLPXyj67jA/8d66eb17bb7d02ca4856ab443a78f2148cafbb129f58a3c81282007c6fe24ff2",
    "description":"",
    "summary":"",
    "artist":"Muffin Man",
    "tags":"",
    "published_at":"2019-09-12T03:00:00.000-04:00",
    "duration":23462,
    "hq":false,
    "guid":"Buzzsprout788880",
    "inactive_at":null,
    "episode_number":4,
    "season_number":5,
    "explicit":true,
    "private":true
  }
]
```
Create episode
-------------
* `POST /episodes.json` will create a new episode with the included parameters.

```json
{
  "title":"Too many or too few?",
  "description":"",
  "summary":"",
  "artist":"Muffin Man",
  "tags":"",
  "published_at":"2019-09-12T03:00:00.000-04:00",
  "duration":23462,
  "hq":false,
  "guid":"Buzzsprout788880",
  "inactive_at":null,
  "episode_number":4,
  "season_number":5,
  "explicit":true,
  "private":true
}
```

This will return `201 Created`,  with the current JSON representation of the episode if the creation was a success.

Update episode
-------------
* `PUT /episodes/12.json` will update an existing episode with the included parameters.

```json
{
  "title":"The New Republic",
  "private":false
}
```

This will return `200 OK` along with the current JSON representation of the updated episode if the creation was a success.
