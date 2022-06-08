---
title: Dangerous Discord API
description: 
published: true
date: 2022-05-26T17:49:19.691Z
tags: 
editor: markdown
dateCreated: 2022-05-26T13:57:03.194Z
---

# API
> Base URL:
[https://dangerousdiscord.com/api](https://dangerousdiscord.com/api)
{.is-info}

## API Key
To use the API, you need an API Key. You can obtain one [here](https://dangerousdiscord.com/profile/api)

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

## API Versions
<ul class="links-list">
  <li>
    <a href="/dangerousdiscord/api/v1" class="is-internal-link">
      Version 1 <em>current</em>
    </a>
  </li>
</ul>
