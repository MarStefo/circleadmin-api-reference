---
description: Endpoints related to User entity
---

# User

{% api-method method="get" host="https://api.admin.circleton.com" path="/user" %}
{% api-method-summary %}
Get Users
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Users successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
[{
    "id": 1,
    "email": "xxx@gmail.com",
    "roles": ["ROLE_ADMIN", "ROLE_SUPER_ADMIN", "ROLE_USER"],
    "name": "xxx",
    "surname": "xxx",
    "birthday": "1997-01-26T00:00:00+00:00",
    "phone": "xxx",
    "address": "xxx",
    "image": "xxx.jpeg",
    "is_deleted": false,
    "credit": 4906.68,
    "phone_verify": "57358",
    "notificationType": 2,
    "createdAt": "2020-09-23T21:00:00+00:00",
    "unsplash_query": "imac",
    "unsplash_photo": {
        "id": "BxCFs6UTQ0Q",
        "width": 6064,
        "height": 4040,
        "description": "Painted on the sidewalk, not sure why but I like it.",
        "alt_description": "Say Hello To Others text",
        "urls": {
            "raw": "https:\/\/images.unsplash.com\/photo-1553404955-af4e8fc7f99f?ixlib=rb-1.2.1\u0026ixid=eyJhcHBfaWQiOjM0NjQ1fQ",
            "full": "https:\/\/images.unsplash.com\/photo-1553404955-af4e8fc7f99f?ixlib=rb-1.2.1\u0026q=85\u0026fm=jpg\u0026crop=entropy\u0026cs=srgb\u0026ixid=eyJhcHBfaWQiOjM0NjQ1fQ",
            "small": "https:\/\/images.unsplash.com\/photo-1553404955-af4e8fc7f99f?ixlib=rb-1.2.1\u0026q=80\u0026fm=jpg\u0026crop=entropy\u0026cs=tinysrgb\u0026w=400\u0026fit=max\u0026ixid=eyJhcHBfaWQiOjM0NjQ1fQ",
            "thumb": "https:\/\/images.unsplash.com\/photo-1553404955-af4e8fc7f99f?ixlib=rb-1.2.1\u0026q=80\u0026fm=jpg\u0026crop=entropy\u0026cs=tinysrgb\u0026w=200\u0026fit=max\u0026ixid=eyJhcHBfaWQiOjM0NjQ1fQ",
            "regular": "https:\/\/images.unsplash.com\/photo-1553404955-af4e8fc7f99f?ixlib=rb-1.2.1\u0026q=80\u0026fm=jpg\u0026crop=entropy\u0026cs=tinysrgb\u0026w=1080\u0026fit=max\u0026ixid=eyJhcHBfaWQiOjM0NjQ1fQ"
        },
        "links": {
            "html": "https:\/\/unsplash.com\/photos\/BxCFs6UTQ0Q",
            "self": "https:\/\/api.unsplash.com\/photos\/BxCFs6UTQ0Q",
            "download": "https:\/\/unsplash.com\/photos\/BxCFs6UTQ0Q\/download",
            "download_location": "https:\/\/api.unsplash.com\/photos\/BxCFs6UTQ0Q\/download"
        },
        "likes": 228,
        "user": {
            "id": "J5RxbqZe0aE",
            "username": "kevin_butz",
            "firstName": "Kevin",
            "lastName": "Butz",
            "links": {
                "html": "https:\/\/unsplash.com\/@kevin_butz",
                "self": "https:\/\/api.unsplash.com\/users\/kevin_butz",
                "likes": "https:\/\/api.unsplash.com\/users\/kevin_butz\/likes",
                "photos": "https:\/\/api.unsplash.com\/users\/kevin_butz\/photos",
                "followers": "https:\/\/api.unsplash.com\/users\/kevin_butz\/followers",
                "following": "https:\/\/api.unsplash.com\/users\/kevin_butz\/following",
                "portfolio": "https:\/\/api.unsplash.com\/users\/kevin_butz\/portfolio"
            }
        }
    },
    "unsplash_createdAt": "2020-10-06T20:43:27+00:00",
    "nomination": "Gentile",
    "gender": "male",
    "quoteId": 5,
    "isWelcomeEnabled": true,
    "isLoginLoggedSuccess": false,
    "isLoginLoggedFail": false,
    "links": [
        {
            "name": "Profilo",
            "url": "https://admin.marstefo.ovh/profile",
            "position": 1
        },
        {
            "name": "Log accessi",
            "url": "https://admin.marstefo.ovh/profile/log",
            "position": 2
        },
        {
            "name": "Account MarStefo",
            "url": "https://account.marstefo.ovh",
            "position": 3
        },
        {
            "name": "Click MarStefo",
            "url": "https://click.marstefo.ovh",
            "position": 4
        },
        {
            "name": "Crowdesk",
            "url": "https://crowdesk.dev",
            "position": 5
        },
        {
            "name": "Dataset MarStefo",
            "url": "https://dataset.marstefo.ovh",
            "position": 6
        },
        {
            "name": "Bike MarStefo",
            "url": "https://bike.marstefo.ovh",
            "position": 7
        },
        {
            "name": "Wemos MarStefo",
            "url": "http://wemos.marstefo.ovh",
            "position": 8
        }
    ],
    "telegramCode": "62935",
    "telegramCodeCreatedAt": "2020-10-06T20:43:24+00:00",
    "telegramData": {
        "id": xxx,
        "lastName": "xxx",
        "username": "xxx",
        "firstName": "xxx"
    },
    "isAllowedToDisableServers": false,
    "limitRefresh": 10,
    "limitRefreshCreatedAt": "2020-09-23T22:00:00+00:00",
    "competency": "Web developer",
    "website": "https:\/\/marstefo.ovh",
    "isPreferringUrlShort": true
}, {
    // [...]
}]


```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.admin.circleton.com" path="/user/team" %}
{% api-method-summary %}
Get Users of the Team CircleTon
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all the users related to the Team CircleTon.  
Users of Team CircleTon are those with ROLE\_BASE \(or inherited\).  
**Please note carefully what is responded, not all fields are given to know.**
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Users successfully retrieved.
{% endapi-method-response-example-description %}

```
[
    {
        "id": 1,
        "name": "xxx",
        "surname": "xxx",
        "competency": "Web developer, student",
        "website": "https://marstefo.ovh"
    },
    {
        "id": 2,
        "name": "xxx",
        "surname": "xxx",
        "competency": "Full stack developer, student",
        "website": "xxx"
    },
    {
       //[...]
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.admin.circleton.com" path="/user" %}
{% api-method-summary %}
Create User
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to create an user.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=true %}
User email
{% endapi-method-parameter %}

{% api-method-parameter name="roles" type="array" required=false %}
Roles \(see role page\)
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
User first name
{% endapi-method-parameter %}

{% api-method-parameter name="surname" type="string" required=false %}
User surname
{% endapi-method-parameter %}

{% api-method-parameter name="birthday" type="string" required=false %}
DateTime ISO 8601 of user birthday
{% endapi-method-parameter %}

{% api-method-parameter name="phone" type="string" required=false %}
User personal telephone number
{% endapi-method-parameter %}

{% api-method-parameter name="address" type="string" required=false %}
User home address
{% endapi-method-parameter %}

{% api-method-parameter name="image" type="string" required=false %}
User profile image \(jpg\). If null remove.
{% endapi-method-parameter %}

{% api-method-parameter name="is\_deleted" type="boolean" required=false %}
Set the user hidden or not
{% endapi-method-parameter %}

{% api-method-parameter name="phone\_verify" type="string" required=false %}
The phone verify code
{% endapi-method-parameter %}

{% api-method-parameter name="notification\_type" type="integer" required=false %}
See User Entity
{% endapi-method-parameter %}

{% api-method-parameter name="createdAt" type="string" required=false %}
DateTime ISO 8601 of user creation 
{% endapi-method-parameter %}

{% api-method-parameter name="unsplash\_query" type="string" required=false %}
The keyword user for Unsplash 
{% endapi-method-parameter %}

{% api-method-parameter name="unsplash\_photo" type="object" required=false %}
See User Entity
{% endapi-method-parameter %}

{% api-method-parameter name="unsplash\_createdAt" type="string" required=false %}
DateTime ISO 8601 of unsplash creation
{% endapi-method-parameter %}

{% api-method-parameter name="nomination" type="string" required=false %}
See User entity
{% endapi-method-parameter %}

{% api-method-parameter name="gender" type="string" required=false %}
See User entity
{% endapi-method-parameter %}

{% api-method-parameter name="quoteId" type="integer" required=false %}
See User entity
{% endapi-method-parameter %}

{% api-method-parameter name="is\_welcome\_enabled" type="boolean" required=false %}
Enable welcome board with photo?
{% endapi-method-parameter %}

{% api-method-parameter name="is\_login\_logged\_success" type="boolean" required=false %}
Enable sending email on login successful?
{% endapi-method-parameter %}

{% api-method-parameter name="is\_login\_logged\_fail" type="boolean" required=false %}
Enable sending email on login failed?
{% endapi-method-parameter %}

{% api-method-parameter name="links" type="array" required=false %}
See User entity
{% endapi-method-parameter %}

{% api-method-parameter name="telegram\_code" type="string" required=false %}
The telegram verify code
{% endapi-method-parameter %}

{% api-method-parameter name="telegram\_code\_createdAt" type="string" required=false %}
DateTime ISO 8601 of telegram verify code creation
{% endapi-method-parameter %}

{% api-method-parameter name="telegram\_data" type="array" required=false %}
Cache of telegram user data. See User entity
{% endapi-method-parameter %}

{% api-method-parameter name="is\_allowed\_to\_disable\_servers" type="boolean" required=false %}
Enable or disable "greedy" mode
{% endapi-method-parameter %}

{% api-method-parameter name="limit\_refresh" type="integer" required=false %}
Limit of servers refresh usages
{% endapi-method-parameter %}

{% api-method-parameter name="limit\_refresh\_created\_at" type="string" required=false %}
DateTime ISO 8601 of limit refresh creation
{% endapi-method-parameter %}

{% api-method-parameter name="competency" type="string" required=false %}
User competency
{% endapi-method-parameter %}

{% api-method-parameter name="website" type="string" required=false %}
User personal website
{% endapi-method-parameter %}

{% api-method-parameter name="is\_preferring\_url\_short" type="boolean" required=false %}
Enable or disable ClickMarStefo integration
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
User successfully created.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 1,
    "email": "xxx@gmail.com",
    "roles": [
        "ROLE_ADMIN",
        "ROLE_SUPER_ADMIN",
        "ROLE_USER"
    ],
    "name": "xxx",
    "surname": "xxx",
    "birthday": "1997-01-26T00:00:00+00:00",
    "phone": "xxx",
    "address": "xxx",
    "image": "xxx.jpeg",
    "is_deleted": false,
    "credit": 4906.68,
    "phone_verify": "57358",
    "notificationType": 2,
    "createdAt": "2020-09-23T21:00:00+00:00",
    "unsplash_query": "imac",
    "unsplash_photo": null,
    "unsplash_createdAt": "2020-10-06T20:43:27+00:00",
    "nomination": "Gentile",
    "gender": "male",
    "quoteId": 5,
    "isWelcomeEnabled": true,
    "isLoginLoggedSuccess": false,
    "isLoginLoggedFail": false,
    "links": [
        {
            "name": "Profilo",
            "url": "https://admin.marstefo.ovh/profile",
            "position": 1
        },
        {
            "name": "Log accessi",
            "url": "https://admin.marstefo.ovh/profile/log",
            "position": 2
        },
        {
            "name": "Account MarStefo",
            "url": "https://account.marstefo.ovh",
            "position": 3
        },
        {
            "name": "Click MarStefo",
            "url": "https://click.marstefo.ovh",
            "position": 4
        },
        {
            "name": "Crowdesk",
            "url": "https://crowdesk.dev",
            "position": 5
        },
        {
            "name": "Dataset MarStefo",
            "url": "https://dataset.marstefo.ovh",
            "position": 6
        },
        {
            "name": "Bike MarStefo",
            "url": "https://bike.marstefo.ovh",
            "position": 7
        },
        {
            "name": "Wemos MarStefo",
            "url": "http://wemos.marstefo.ovh",
            "position": 8
        }
    ],
    "telegramCode": "62935",
    "telegramCodeCreatedAt": "2020-10-06T20:43:24+00:00",
    "telegramData": null,
    "isAllowedToDisableServers": false,
    "limitRefresh": 10,
    "limitRefreshCreatedAt": "2020-09-23T22:00:00+00:00",
    "competency": "Web developer",
    "website": "https://marstefo.ovh",
    "isPreferringUrlShort": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.admin.circleton.com" path="/user/:user" %}
{% api-method-summary %}
Get User
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get the specified user ID.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user" type="integer" required=true %}
User ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
User successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 1,
    "email": "xxx@gmail.com",
    "roles": [
        "ROLE_ADMIN",
        "ROLE_SUPER_ADMIN",
        "ROLE_USER"
    ],
    "name": "xxx",
    "surname": "xxx",
    "birthday": "1997-01-26T00:00:00+00:00",
    "phone": "xxx",
    "address": "xxx",
    "image": "xxx.jpeg",
    "is_deleted": false,
    "credit": 4906.68,
    "phone_verify": "57358",
    "notificationType": 2,
    "createdAt": "2020-09-23T21:00:00+00:00",
    "unsplash_query": "imac",
    "unsplash_photo": null,
    "unsplash_createdAt": "2020-10-06T20:43:27+00:00",
    "nomination": "Gentile",
    "gender": "male",
    "quoteId": 5,
    "isWelcomeEnabled": true,
    "isLoginLoggedSuccess": false,
    "isLoginLoggedFail": false,
    "links": [
        {
            "name": "Profilo",
            "url": "https://admin.marstefo.ovh/profile",
            "position": 1
        },
        {
            "name": "Log accessi",
            "url": "https://admin.marstefo.ovh/profile/log",
            "position": 2
        },
        {
            "name": "Account MarStefo",
            "url": "https://account.marstefo.ovh",
            "position": 3
        },
        {
            "name": "Click MarStefo",
            "url": "https://click.marstefo.ovh",
            "position": 4
        },
        {
            "name": "Crowdesk",
            "url": "https://crowdesk.dev",
            "position": 5
        },
        {
            "name": "Dataset MarStefo",
            "url": "https://dataset.marstefo.ovh",
            "position": 6
        },
        {
            "name": "Bike MarStefo",
            "url": "https://bike.marstefo.ovh",
            "position": 7
        },
        {
            "name": "Wemos MarStefo",
            "url": "http://wemos.marstefo.ovh",
            "position": 8
        }
    ],
    "telegramCode": "62935",
    "telegramCodeCreatedAt": "2020-10-06T20:43:24+00:00",
    "telegramData": null,
    "isAllowedToDisableServers": false,
    "limitRefresh": 10,
    "limitRefreshCreatedAt": "2020-09-23T22:00:00+00:00",
    "competency": "Web developer",
    "website": "https://marstefo.ovh",
    "isPreferringUrlShort": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



{% api-method method="put" host="https://api.admin.circleton.com" path="/user/:user" %}
{% api-method-summary %}
Edit user
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to edit the specified user ID.   
**Values are updated if provided.**
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user" type="integer" required=true %}
User ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
User email
{% endapi-method-parameter %}

{% api-method-parameter name="roles" type="array" required=false %}
Roles \(see role page\)
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
User first name
{% endapi-method-parameter %}

{% api-method-parameter name="surname" type="string" required=false %}
User surname
{% endapi-method-parameter %}

{% api-method-parameter name="birthday" type="string" required=false %}
DateTime ISO 8601 of user birthday
{% endapi-method-parameter %}

{% api-method-parameter name="phone" type="string" required=false %}
User personal telephone number
{% endapi-method-parameter %}

{% api-method-parameter name="address" type="string" required=false %}
User home address
{% endapi-method-parameter %}

{% api-method-parameter name="image" type="string" required=false %}
User profile image \(jpg\). If null remove.
{% endapi-method-parameter %}

{% api-method-parameter name="is\_deleted" type="boolean" required=false %}
Set the user hidden or not
{% endapi-method-parameter %}

{% api-method-parameter name="phone\_verify" type="string" required=false %}
The phone verify code
{% endapi-method-parameter %}

{% api-method-parameter name="notification\_type" type="integer" required=false %}
See User Entity
{% endapi-method-parameter %}

{% api-method-parameter name="createdAt" type="string" required=false %}
DateTime ISO 8601 of user creation 
{% endapi-method-parameter %}

{% api-method-parameter name="unsplash\_query" type="string" required=false %}
The keyword user for Unsplash 
{% endapi-method-parameter %}

{% api-method-parameter name="unsplash\_photo" type="object" required=false %}
See User Entity
{% endapi-method-parameter %}

{% api-method-parameter name="unsplash\_createdAt" type="string" required=false %}
DateTime ISO 8601 of unsplash creation
{% endapi-method-parameter %}

{% api-method-parameter name="nomination" type="string" required=false %}
See User entity
{% endapi-method-parameter %}

{% api-method-parameter name="gender" type="string" required=false %}
See User entity
{% endapi-method-parameter %}

{% api-method-parameter name="quoteId" type="integer" required=false %}
See User entity
{% endapi-method-parameter %}

{% api-method-parameter name="is\_welcome\_enabled" type="boolean" required=false %}
Enable welcome board with photo?
{% endapi-method-parameter %}

{% api-method-parameter name="is\_login\_logged\_success" type="boolean" required=false %}
Enable sending email on login successful?
{% endapi-method-parameter %}

{% api-method-parameter name="is\_login\_logged\_fail" type="boolean" required=false %}
Enable sending email on login failed?
{% endapi-method-parameter %}

{% api-method-parameter name="links" type="array" required=false %}
See User entity
{% endapi-method-parameter %}

{% api-method-parameter name="telegram\_code" type="string" required=false %}
The telegram verify code
{% endapi-method-parameter %}

{% api-method-parameter name="telegram\_code\_createdAt" type="string" required=false %}
DateTime ISO 8601 of telegram verify code creation
{% endapi-method-parameter %}

{% api-method-parameter name="telegram\_data" type="array" required=false %}
Cache of telegram user data. See User entity
{% endapi-method-parameter %}

{% api-method-parameter name="is\_allowed\_to\_disable\_servers" type="boolean" required=false %}
Enable or disable "greedy" mode
{% endapi-method-parameter %}

{% api-method-parameter name="limit\_refresh" type="integer" required=false %}
Limit of servers refresh usages
{% endapi-method-parameter %}

{% api-method-parameter name="limit\_refresh\_created\_at" type="string" required=false %}
DateTime ISO 8601 of limit refresh creation
{% endapi-method-parameter %}

{% api-method-parameter name="competency" type="string" required=false %}
User competency
{% endapi-method-parameter %}

{% api-method-parameter name="website" type="string" required=false %}
User personal website
{% endapi-method-parameter %}

{% api-method-parameter name="is\_preferring\_url\_short" type="boolean" required=false %}
Enable or disab
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
User successfully edited.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 1,
    "email": "xxx@gmail.com",
    "roles": [
        "ROLE_ADMIN",
        "ROLE_SUPER_ADMIN",
        "ROLE_USER"
    ],
    "name": "xxx",
    "surname": "xxx",
    "birthday": "1997-01-26T00:00:00+00:00",
    "phone": "xxx",
    "address": "xxx",
    "image": "xxx.jpeg",
    "is_deleted": false,
    "credit": 4906.68,
    "phone_verify": "57358",
    "notificationType": 2,
    "createdAt": "2020-09-23T21:00:00+00:00",
    "unsplash_query": "imac",
    "unsplash_photo": null,
    "unsplash_createdAt": "2020-10-06T20:43:27+00:00",
    "nomination": "Gentile",
    "gender": "male",
    "quoteId": 5,
    "isWelcomeEnabled": true,
    "isLoginLoggedSuccess": false,
    "isLoginLoggedFail": false,
    "links": [
        {
            "name": "Profilo",
            "url": "https://admin.marstefo.ovh/profile",
            "position": 1
        },
        {
            "name": "Log accessi",
            "url": "https://admin.marstefo.ovh/profile/log",
            "position": 2
        },
        {
            "name": "Account MarStefo",
            "url": "https://account.marstefo.ovh",
            "position": 3
        },
        {
            "name": "Click MarStefo",
            "url": "https://click.marstefo.ovh",
            "position": 4
        },
        {
            "name": "Crowdesk",
            "url": "https://crowdesk.dev",
            "position": 5
        },
        {
            "name": "Dataset MarStefo",
            "url": "https://dataset.marstefo.ovh",
            "position": 6
        },
        {
            "name": "Bike MarStefo",
            "url": "https://bike.marstefo.ovh",
            "position": 7
        },
        {
            "name": "Wemos MarStefo",
            "url": "http://wemos.marstefo.ovh",
            "position": 8
        }
    ],
    "telegramCode": "62935",
    "telegramCodeCreatedAt": "2020-10-06T20:43:24+00:00",
    "telegramData": null,
    "isAllowedToDisableServers": false,
    "limitRefresh": 10,
    "limitRefreshCreatedAt": "2020-09-23T22:00:00+00:00",
    "competency": "Web developer",
    "website": "https://marstefo.ovh",
    "isPreferringUrlShort": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://api.admin.circleton.com" path="/user/:user" %}
{% api-method-summary %}
Delete User
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user" type="integer" required=true %}
User ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}
User successfully deleted.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

