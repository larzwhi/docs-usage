+++
weight = 7
date = "2014-11-08T12:54:12-08:00"
title = "Webhook"

[menu.docs]
parent = "Notify"
+++

Webhook notifications

```coffeescript
notify:
  webhook:
    urls:
      - "http://foo.com/hook/url"
    on_success: true
    on_failure: true
```

Below is an example payload that you can expect:

```json
{
  "from_url": "http://drone.foo.com",
  "repository": {
    "remote": "github.com",
    "host": "github.com",
    "owner": "foo",
    "name": "bar",
    "url": "https:\/\/github.com\/foo\/bar",
    "clone_url": "git@github.com:foo\/bar.git",
    "git_url": "git:\/\/github.com\/foo\/bar.git",
    "ssh_url": "git@github.com:foo\/bar.git",
    "active": false,
    "private": true,
    "privileged": false,
    "post_commits": false,
    "pull_requests": false,
    "timeout": 900,
    "created_at": 1413339970,
    "updated_at": 1413339970
  },
  "commit": {
    "id": 327,
    "status": "Success",
    "started_at": 1421029603,
    "finished_at": 1421029813,
    "duration": 210,
    "sha": "9f2849d5adf2aa47745e1b7b9f76f1fcca1ebdb3",
    "branch": "master",
    "pull_request": "800",
    "author": "john.smith@gmail.com",
    "gravatar": "0bb3b7d4301b9e1335c6910f86362194",
    "timestamp": "2015-01-12 02:21:54.959678775 +0000 UTC",
    "message": "Update the Readme",
    "created_at": 1421029315,
    "updated_at": 1421029813
  }
}
```
