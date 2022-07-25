---
title: User | v1
description: 
published: true
date: 2022-07-25T21:14:59.176Z
tags: 
editor: markdown
dateCreated: 2022-05-27T10:45:00.217Z
---

# API v1

> Base URL:
[https://discord.drivet.xyz/api/v1](https://discord.drivet.xyz/api/v1)
{.is-info}

# Objects

## User Object
| field         | type                          | description                                                     |
|---------------|-------------------------------|-----------------------------------------------------------------|
| id            | snowflake                     | the user's id                                                   |
| username      | string                        | the user's name                                                 |
| avatar        | ?string                       | the user's avatar hash                                          |
| discriminator | string                        | the user's 4-digit discord tag                                  |
| reports       | integer                       | shows how many times the user has been reported                 |
| badges?       | [badges](#user-badges) object | an object containing the user badges                            |
| votes         | [votes](#user-votes) object   | an object containing the user votes                             |
| flags         | [flags](#user-flags) object   | an object containing some user flags provided by Discord                             |

## User badges
| field        | type    | description                                               |
|--------------|---------|-----------------------------------------------------------|
| blacklisted? | boolean | whether the user is blacklisted                           |
| whitelisted? | boolean | whether the user is whitelisted                           |
| admin?       | boolean | whether the user is an Administrator on Dangerous Discord |
| raid_bot?    | boolean | whether the user has been detected as a raid bot by Dangerous Discord's automation |

## User votes
| field     | type    | description                   |
|-----------|---------|-------------------------------|
| upvotes   | integer | integer of upvotes recieved   |
| downvotes | integer | integer of downvotes received |

## User flags
| field     | type    | description                                         |
|-----------|---------|-----------------------------------------------------|
| spammer   | boolean | whether the user is flagged as a spammer by Discord |
| downvotes | integer | integer of downvotes received                       |

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
| field    | type    | description                                                                         | default |
|----------|---------|-------------------------------------------------------------------------------------|---------|
| author   | string  | The author of the report, this field requires a [**TRUSTED TOKEN**](#trusted-tokens)| -       |
| category | integer | A category integer from [category choices](#category-choices)                       | 0       |
| reason   | string  | Report's reason. Minimum 10 characters                                              | -       |

<br>

> Trying to use the `author` field without an Trusted Token will result in an `403` error!
{.is-warning}

### Category choices
- Other: `0`
- Advertising: `1`
- Spamming: `2`
- Raiding: `3`
- Harassing: `4`

## Trusted Tokens
An trusted token is given only to trusted users, they are provided directly by the **Dangerous Discord** staff!
