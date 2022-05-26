---
title: v1 User
description: 
published: true
date: 2022-05-26T16:31:37.233Z
tags: 
editor: markdown
dateCreated: 2022-05-26T15:33:08.296Z
---

# API v1

> Base URL:
[https://discord.drivet.xyz/api/v1](https://discord.drivet.xyz/api/v1)
{.is-info}

# Objects

## User Object
| field         | type      | description                                     |
|---------------|-----------|-------------------------------------------------|
| id            | snowflake | the user's id                                   |
| username      | string    | the user's name                                 |
| avatar        | ?string   | the user's avatar hash                          |
| discriminator | string    | the user's 4-digit discord tag                  |
| reports       | integer   | Shows how many times the user has been reported |
| badges?       | array     | an array of [badges](#user-badges)              |
| votes         | array     | an array of [votes](#user-votes)                |

## User badges
| field        | type    | description                                               |
|--------------|---------|-----------------------------------------------------------|
| blacklisted? | boolean | whether the user is blacklisted                           |
| whitelisted? | boolean | whether the user is whitelisted                           |
| admin?       | boolean | whether the user is an Administrator on Dangerous Discord |

## User votes
| field     | type    | description                   |
|-----------|---------|-------------------------------|
| upvotes   | integer | integer of upvotes recieved   |
| downvotes | integer | integer of downvotes received |

# Resources

## Get Current User
`GET` /user/@me

Returns a [user](#user-object) object of the requester account.

## Get User
`GET` /user/:user_id

Returns a [user](#user-object) object for a given user ID.

## Report User
`POST` /user/:user_id/report

<br>

### JSON Params
| field    | type    | description                                                   | default |
|----------|---------|---------------------------------------------------------------|---------|
| category | integer | A category integer from [category choices](#category-choices) | 0       |
| reason   | string  | Report's reason. Minimum 10 characters                        | -       |

<br>

### Category choices
- Other: `0`
- Advertising: `1`
- Spamming: `2`
- Raiding: `3`
- Harassing: `4`