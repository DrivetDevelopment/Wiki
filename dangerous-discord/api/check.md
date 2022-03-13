---
title: Dangerous Discord API - Check a user
description: 
published: true
date: 2022-03-13T16:21:10.612Z
tags: 
editor: markdown
dateCreated: 2022-03-13T16:21:00.128Z
---

# Check the reports of a user using the API
> This is a "API" documentation for developers. If you are just a regular user, please visit https://dangerousdiscord.com
{.is-info}

## Step 1
Send a GET request to `https://dangerousdiscord.com/api/check` and add the User ID as a param `?id=267386908382855169`.
You should get a response back like this:
```json
{
  "reports": 0,
  "users_reported": 0,
  "blacklisted": false,
  "whitelisted": true
}
```

## Step 2
Voilà
