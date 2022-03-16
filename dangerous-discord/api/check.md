---
title: Dangerous Discord API - Check a user
description: 
published: true
date: 2022-03-16T14:16:33.495Z
tags: 
editor: markdown
dateCreated: 2022-03-13T15:32:41.998Z
---

# Check the reports of a user using the API
> This is a "API" documentation for developers. If you are just a regular user, please visit https://dangerousdiscord.com
{.is-info}

Send a GET request to `https://discord.drivet.xyz/api/check` and add the User ID as a "id" parameter, for example: `?id=267386908382855169`.

Full URL: https://dangerousdiscord.com/api/check?id=267386908382855169

You should get a response back like this:
```json
{
  "reports": 0,
  "users_reported": 0,
  "blacklisted": false,
  "whitelisted": true
}
```
