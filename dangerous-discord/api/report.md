---
title: Dangerous Discord API - Report a user
description: 
published: true
date: 2022-03-11T18:59:28.612Z
tags: 
editor: markdown
dateCreated: 2022-01-30T14:58:25.719Z
---

# Report a user using the API
> This is a "API" documentation for developers. If you are just a regular user, please visit https://dangerousdiscord.com
{.is-info}


## Step 1
Skip this step if you already have an API key

Login to [Dangerous Discord](https://dangerousdiscord.com) and then head to the [API page](https://dangerousdiscord.com/profile/api). Click on the `Get an API key` button

![dd-api-key.png](/dd-api-key.png)

## Step 2
Send a POST request to `https://dangerousdiscord.com/api/report` with the following example body:
```json
{
    "token": "dd._0MpykT1Mtq7wWRDblNoZ4bGuTEF9MXE9",
    "id": "267386908382855169",
  	"type": "this is optional but valid ones are: Advertising, Spamming, Raiding, Harassing, Other",
  	"reason": "Racist"
}
```

## Step 3
Voilà