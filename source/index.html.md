---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript

includes:
  # - errors

search: true

code_clipboard: true

# meta:
#   - name: description
#     content: Documentation for the Kittn API
---

# Introduction

Bienvenidos amigos! Here you can find the documentation for Qmend's REST API. 

# Authentication


For authentication, we use Laravel Sanctum. To authenticate SPAs, follow [Laravel's doumentation](https://laravel.com/docs/9.x/sanctum#spa-authentication).

# Businesses

## Get Businesses

> The response JSON will be structured like this:

```json

{
  "id": 2,
  "name": "Walker, Parisian and McDermott",
  "status": 1,
  "phone_number": "843-915-0927",
  "address": "72245 Timothy Ford Suite 906\nMitchellstad, NJ 78606",
  "zipcode": "88895-1724",
  "city_id": 126,
  "state_id": "WA",
  "country_id": 1,
  "lat": "31.3819",
  "lng": "-37.1335",
  "created_at": "2022-08-23T20:48:51.000000Z",
  "updated_at": "2022-08-23T20:48:51.000000Z",
  "reviews": [
    {
      "id": 27,
      "business_id": 2,
      "source_id": 1,
      "number_of_reviews": 305,
      "score": 1.4,
      "link": "https://www.google.com/maps/place/Siena+Tavern/@41.8890864,-87.6298924,15z/data=!3m1!5s0x880e2cb74cae0e7b:0xb7392f617178520d!4m7!3m6!1s0x0:0xecd6f9b48656e27b!8m2!3d41.8890864!4d-87.6298924!9m1!1b1",
      "created_at": "2022-08-23T20:50:48.000000Z",
      "updated_at": "2022-08-23T20:50:48.000000Z",
      "source": {
        "id": 1,
        "name": "Google",
        "created_at": "2022-08-23T20:43:31.000000Z",
        "updated_at": "2022-08-23T20:43:31.000000Z"
      }
    },
    {
      "id": 99,
      "business_id": 2,
      "source_id": 2,
      "number_of_reviews": 1320,
      "score": 3.4,
      "link": "https://www.google.com/maps/place/Siena+Tavern/@41.8890864,-87.6298924,15z/data=!3m1!5s0x880e2cb74cae0e7b:0xb7392f617178520d!4m7!3m6!1s0x0:0xecd6f9b48656e27b!8m2!3d41.8890864!4d-87.6298924!9m1!1b1",
      "created_at": "2022-08-23T20:50:58.000000Z",
      "updated_at": "2022-08-23T20:50:58.000000Z",
      "source": {
        "id": 2,
        "name": "Yelp",
        "created_at": "2022-08-23T20:43:31.000000Z",
        "updated_at": "2022-08-23T20:43:31.000000Z"
      }
    },
    {
      "id": 80,
      "business_id": 2,
      "source_id": 3,
      "number_of_reviews": 163,
      "score": 1.5,
      "link": "https://www.google.com/maps/place/Siena+Tavern/@41.8890864,-87.6298924,15z/data=!3m1!5s0x880e2cb74cae0e7b:0xb7392f617178520d!4m7!3m6!1s0x0:0xecd6f9b48656e27b!8m2!3d41.8890864!4d-87.6298924!9m1!1b1",
      "created_at": "2022-08-23T20:50:52.000000Z",
      "updated_at": "2022-08-23T20:50:52.000000Z",
      "source": {
        "id": 3,
        "name": "Tripadvisor",
        "created_at": "2022-08-23T20:43:31.000000Z",
        "updated_at": "2022-08-23T20:43:31.000000Z"
      }
    },
    {
      "id": 64,
      "business_id": 2,
      "source_id": 4,
      "number_of_reviews": 1863,
      "score": 2.3,
      "link": "https://www.google.com/maps/place/Siena+Tavern/@41.8890864,-87.6298924,15z/data=!3m1!5s0x880e2cb74cae0e7b:0xb7392f617178520d!4m7!3m6!1s0x0:0xecd6f9b48656e27b!8m2!3d41.8890864!4d-87.6298924!9m1!1b1",
      "created_at": "2022-08-23T20:50:52.000000Z",
      "updated_at": "2022-08-23T20:50:52.000000Z",
      "source": {
        "id": 4,
        "name": "Grubhub",
        "created_at": "2022-08-23T20:43:31.000000Z",
        "updated_at": "2022-08-23T20:43:31.000000Z"
      }
    },
    {
      "id": 44,
      "business_id": 2,
      "source_id": 5,
      "number_of_reviews": 1073,
      "score": 3.1,
      "link": "https://www.google.com/maps/place/Siena+Tavern/@41.8890864,-87.6298924,15z/data=!3m1!5s0x880e2cb74cae0e7b:0xb7392f617178520d!4m7!3m6!1s0x0:0xecd6f9b48656e27b!8m2!3d41.8890864!4d-87.6298924!9m1!1b1",
      "created_at": "2022-08-23T20:50:50.000000Z",
      "updated_at": "2022-08-23T20:50:50.000000Z",
      "source": {
        "id": 5,
        "name": "OpenTable",
        "created_at": "2022-08-23T20:43:31.000000Z",
        "updated_at": "2022-08-23T20:43:31.000000Z"
      }
    }
  ],
  "hoursofoperations": [
    {
      "id": 41,
      "business_id": 2,
      "open_time": "12:00 a.m.",
      "close_time": "8:00 p.m.",
      "day": "Monday",
      "created_at": "2022-08-23T20:52:08.000000Z",
      "updated_at": "2022-08-23T20:52:08.000000Z"
    },
    {
      "id": 6,
      "business_id": 2,
      "open_time": "10:00 a.m.",
      "close_time": "11:00 p.m.",
      "day": "Sunday",
      "created_at": "2022-08-23T20:51:30.000000Z",
      "updated_at": "2022-08-23T20:51:30.000000Z"
    },
    {
      "id": 33,
      "business_id": 2,
      "open_time": "7:00 a.m.",
      "close_time": "8:00 p.m.",
      "day": "Tuesday",
      "created_at": "2022-08-23T20:51:52.000000Z",
      "updated_at": "2022-08-23T20:51:52.000000Z"
    }
  ]
}
```

This endpoint retrieves all businesses if no query parameter is provided. Use a query parameter to get specific business(es).

### HTTP Request

`GET https://qmend.com/api/business`

### Query Parameters

Parameter | Default | Description | Type
--------- | ------- | ----------- | ----
name | N/A | If name is given, the query will return a result of all businesses that match any part of the value provided. | String
business_id | N/A | Returns business assigned to business_id. | Int
status | N/A | Returns all businesses with status value.  | Boolean
zipcode | N/A | Returns all businesses with zipcode value. | Int
city_id | N/A | Returns all businesses with city_id value. | Int
state_id | N/A | Returns all businesses with state_id value. Use a state's 2 letter abbreviation. | String


<aside class="success">
A combination of the listed parameters can be used for more specific results.
</aside>
