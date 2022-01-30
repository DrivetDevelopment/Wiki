---
title: Dangerous Discord API - Report a user
description: 
published: true
date: 2022-01-30T14:58:31.870Z
tags: 
editor: markdown
dateCreated: 2022-01-30T14:58:25.719Z
---

# Report a user using the API
> This is a "API" documentation for developers. If you are just a regular user, please visit https://discord.drivet.xyz
{.is-info}


## Step 1
Skip this step if you already have an API key

Login to [Dangerous Discord](https://discord.drivet.xyz) and then head to the [API page](https://discord.drivet.xyz/profile/api). Click on the `Get an API key` button

![image.png](/image.png)

## Step 2
Send a POST request to `https://discord.drivet.xyz/api/report` with the following example body:
```json
{
    "token": "dd._0MpykT1Mtq7wWRDblNoZ4bGuTEF9MXE9",
    "id": "267386908382855169",
  	"type": "this is optional but valid ones are: Advertising, Spamming, Raiding, Harassing, Other".
  	"reason": "Racist"
}
```

## Step 3
Voilà