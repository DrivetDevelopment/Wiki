---
title: Dangerous Discord API
description: 
published: true
date: 2022-05-26T15:19:37.679Z
tags: 
editor: markdown
dateCreated: 2022-05-26T13:57:03.194Z
---

# API
> Base URL:
[https://discord.drivet.xyz/api](https://discord.drivet.xyz/api)
{.is-info}

## API Key
To use the API, you need an API Key. You can obtain one [here](https://discord.drivet.xyz/profile/api)

For every API route, your request must have the `Authorization` header as a `Bearer` key
```
Authorization: Bearer dd._FJ349...JHYF6ipnOOR
```

## Error responses
Errors always returns a object that looks like the one below.
```
{ 
	error: true,
	code: 400, 
	message: 'User ID must be a number only'
}
```