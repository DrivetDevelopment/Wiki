---
title: URL Shortener - Add Links
description: 
published: true
date: 2022-05-25T13:06:47.260Z
tags: 
editor: markdown
dateCreated: 2022-05-25T13:06:45.286Z
---

# Add Links to URL Shortener
> Drivet URL Shortener does not exist anymore, and we have no plans to bring it back until further notice. Feel free to give feedback regarding this via email [aleksi@drivet.xyz](mailto:aleksi@drivet.xyz).
{.is-danger}

This tutorial will help you to shorten urls using Drivet's URL Shortener

> This is a "API" documentation for developers. Please visit https://shorten.drivet.xyz to create urls faster.
{.is-info}


> Drivet's URL Shortener is not a IP logger. Though people who create links have the possibility to redirect to a IP Logger. Use https://wheregoes.com/ to check where the link goes if you doubt something.
{.is-info}

> If you have found any links that redirects to IP loggers, contact us at [aleksi@drivet.xyz](mailto:aleksi@drivet.xyz) and we will sort it out
{.is-info}


## Step 1
Send a `POST` request to `https://r.drivet.xyz` with the following body:
```json
{
	"url": "https://www.reuters.com/technology/google-services-down-some-users-downdetector-2021-06-29/"
}
```
## Step 2
Copy the url you got by sending the request above
```json
{
    "shortcode": "nDbLks",
    "url": "https://r.drivet.xyz/nDbLks"
}
```

The link `https://r.drivet.xyz/wg8XAg` now will redirect to `https://www.reuters.com/technology/google-services-down-some-users-downdetector-2021-06-29/`