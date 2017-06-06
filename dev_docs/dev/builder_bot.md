---
title: Builder Bot
layout: longpage
permalink: /dev_docs/dev/builder_bot/
---
Bot Account: https://github.com/tripleabuilderbot

## Overview

An admin owned account used for automated build tasks that require repository write access.


## Personal Access Keys

- Travis automated releases key
  - Usage: https://github.com/triplea-game/triplea/blob/master/.travis.yml#L32)
    Description: This key allows travis to push to github releases. It is set up by the
      travis ruby set up program when first configuring travis with triplea.
- Map Push Key
  - Usage: https://github.com/triplea-game/triplea/blob/master/.travis/push_maps_yaml#L10
    Description: Write-Access to triplea github.io website repo to add map description files
- Push Tag
  - Usage: https://github.com/triplea-game/triplea/blob/master/.travis/push_tag#L13
    Description: write permission to triplea repo for creating a new tag on each release.
      The tags are primarily for convenience, so we can relatively easily checkout a specific
      version that we released. This is also a carry-over of the process TripleA used when
      hosted in SVN.

Snapshot:

![tokens](https://cloud.githubusercontent.com/assets/12397753/26811743/822517d6-4a28-11e7-8342-ef4826e834b9.png)



## Travis Config:

The key values are recorded in travis as env variable values. They are write-once only. To regenerate them, regenerate the
key in github, delete the existing key in travis and recreate it with the newly known key value.

Config is here (Must be logged in as the botor with admin/write access to triplea): https://travis-ci.org/triplea-game/triplea/settings

Snapshot:
![travis](https://cloud.githubusercontent.com/assets/12397753/26811735/6e69c5de-4a28-11e7-8996-49338f428349.png)



## Tips

- Using 'private' mode browsing is useful when logging in as the bot account.