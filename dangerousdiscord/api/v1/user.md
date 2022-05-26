---
title: v1 User
description: 
published: true
date: 2022-05-26T15:53:49.668Z
tags: 
editor: markdown
dateCreated: 2022-05-26T15:33:08.296Z
---

# API v1

> Base URL:
[https://discord.drivet.xyz/api/v1](https://discord.drivet.xyz/api/v1)
{.is-info}

# Resources

## Get Current User
`GET` /user/@me

## Get User
`GET` /user/:user_id

## Report User
`POST` /user/:user_id/report

<br>

### JSON Params
| field    | type   | description                                           | default |
|----------|--------|-------------------------------------------------------|---------|
| category | string | A category from [category choices](#category-choices) | Other   |
| reason   | string | Report's reason. Minimum 10 characters                | -       |

<br>

### Category choices
- Advertising
- Spamming
- Raiding
- Harassing
- Other

# Reference

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