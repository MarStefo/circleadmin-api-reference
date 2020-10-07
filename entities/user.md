---
description: Specifications for the User entity
---

# User

## Summary

| **field** | **type** | default |
| :--- | :--- | :--- |
| id | int |  |
| email | string |  |
| roles | json |  |
| ~~password~~ | ~~string~~ |  |
| name | string |  |
| surname | string |  |
| birthday | date |  |
| phone | string |  |
| address | text |  |
| image | string |  |
| is\_deleted | bool | false |
| credit | int | 0 |
| ~~wizard\_status~~ | ~~int~~ |  |
| phone\_verify | string |  |
| notification\_type | int |  |
| created\_at | datetime | now |
| unsplash\_query | string |  |
| unsplash\_photo | json |  |
| unsplash\_created\_at | datetime |  |
| nomination | string | NOMINATION\_DEFAULT = "Gentile" |
| gender | string |  |
| quote\_id | int | 5 |
| is\_welcome\_enabled | bool | true |
| is\_login\_logged\_success | bool | true |
| is\_login\_logged\_fail | bool | true |
| ~~is\_disabled\_cookies~~ | ~~bool~~ |  |
| links | json | _see default value at description field_ |
| telegram\_code | string |  |
| telegram\_code\_created\_at | datetime |  |
| telegram\_data | json |  |
| ~~fast\_lane\_token~~ | ~~string~~ |  |
| ~~fast\_lane\_token\_created\_at~~ | ~~datetime~~ |  |
| ~~reset\_password\_code~~ | ~~string~~ |  |
| ~~reset\_password\_created\_at~~ | ~~datetime~~ |  |
| is\_allowed\_to\_disable\_servers | bool | false |
| limit\_refresh | int | LIMIT\_REFRESH\_DEFAULT = 10 |
| limit\_refresh\_created\_at | datetime | now |
| competency | text |  |
| website | text |  |
| is\_preferring\_url\_short | bool | true |

### Field **`id` `(int)`**

The identifier of the user.

### Field **`email` `(string)`**

The email of the user.

### Field **`roles` `(json)`**

The roles of the user. For more information read the Roles page.

{% page-ref page="../extra/roles.md" %}

### Field **`password` `(string)`**

{% hint style="danger" %}
**This field is deprecated and must not be included!**
{% endhint %}

The password of the user in a Symfony format \(using encoder _Symfony\Component\Security\Core\Encoder\MigratingPasswordEncoder_\), [read more](https://symfony.com/doc/current/security.html#c-encoding-passwords).  
Example with "password":

```text
$argon2id$v=19$m=65536,t=4,p=1$U9abNvLaxePNJ5H88iKVRA$PIGx9ud4kydodQbaBMOqotCuOkj5rCqtHWrybwY4JsU
```

{% hint style="info" %}
To authenticate the user in project != Symfony, we suggest you to use POauth: [https://poauth.it](https://poauth.it)
{% endhint %}

### Field **`name` `(string)`**

The name of the user.

### Field **`surname` `(string)`**

The surname of the user.

### Field `birthday` **`(date)`**

The birtday of the user in MySQL DATE format.

### Field **`phone` `(string)`**

The phone number of the user.

### Field **`address` `(text)`**

The home address of the user.

### Field **`image` `(string)`**

The local path of image profile.

{% hint style="info" %}
The full path is:   
https://adminv3.slobodiuk.vm.marstefo.ovh/img/users/{local path of the image}  
If `image` is null, the default one is:  
[https://adminv3.slobodiuk.vm.marstefo.ovh/img/default.png](https://adminv3.slobodiuk.vm.marstefo.ovh/img/default.png)
{% endhint %}

### Field **`is_deleted` `(bool)`**

If the user is deleted, he cannot login \(and also in POauth\), but all his data is untoched.

### Field **`credit` `(int)`**

The calculated value of credit.

{% hint style="danger" %}
Never change this field directly in APIs. This value is calculated and can be changed only indirectly by functions used to pay and to add credit.
{% endhint %}

{% hint style="info" %}
**Please save all monetary values multiplied by 100. Return to API already divided by 100.**
{% endhint %}

### Field **`wizard_status` `(int)`**

{% hint style="danger" %}
**This field is deprecated and must not be included!**
{% endhint %}

Service value to detect the step of the initial wizard. To disable set to -1.

| value | comment |
| :--- | :--- |
| 0 |  WIZARD\_NEW |
| 1 | WIZARD\_REGISTRY |
| 2 | WIZARD\_CONTACTS |
| 3 | WIZARD\_CONTACTS\_VERIFY |
| 4 | WIZARD\_COMMUNICATIONS |
| 5 | WIZARD\_CONCLUSION |
| -1 | WIZARD\_END |

### Field **`phone_verify` `(string)`**

The value of the sms verification code.

### Field **`notification_type` `(int)`**

This value is the preferred option of the communication type chosen by the user.

| value | comment |
| :--- | :--- |
| 0 | NOTIFICATION\_NO\_NOTIFICATION |
| 1 | NOTIFICATION\_INFO |
| 2 | NOTIFICATION\_INFO\_ADMIN |

### Field **`created_at` `(datetime)`**

The MySQL DATETIME of creation of the user.

{% hint style="info" %}
If it is NULL, the user is registered as "_import from old management software_".
{% endhint %}

### Field **`unsplash_query` `(string)`**

The query used to search a unsplash photo.

### Field **`unsplash_photo` `(json)`**

The rapresentation of a object that contains the photo cache. This value is resetted every night at 00.00.  
Example of content:

```text
{
	"id": "N4bE30MecGk",
	"urls": {
		"raw": "https://images.unsplash.com/photo-1533212026022-d1affe8cc6dd?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjM0NjQ1fQ",
		"full": "https://images.unsplash.com/photo-1533212026022-d1affe8cc6dd?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&ixid=eyJhcHBfaWQiOjM0NjQ1fQ",
		"small": "https://images.unsplash.com/photo-1533212026022-d1affe8cc6dd?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=400&fit=max&ixid=eyJhcHBfaWQiOjM0NjQ1fQ",
		"thumb": "https://images.unsplash.com/photo-1533212026022-d1affe8cc6dd?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=200&fit=max&ixid=eyJhcHBfaWQiOjM0NjQ1fQ",
		"regular": "https://images.unsplash.com/photo-1533212026022-d1affe8cc6dd?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjM0NjQ1fQ"
	},
	"user": {
		"id": "CqFZXSlanxA",
		"links": {
			"html": "https://unsplash.com/@devano23",
			"self": "https://api.unsplash.com/users/devano23",
			"likes": "https://api.unsplash.com/users/devano23/likes",
			"photos": "https://api.unsplash.com/users/devano23/photos",
			"followers": "https://api.unsplash.com/users/devano23/followers",
			"following": "https://api.unsplash.com/users/devano23/following",
			"portfolio": "https://api.unsplash.com/users/devano23/portfolio"
		},
		"lastName": "Janse van Rensburg",
		"linkHtml": "https://unsplash.com/@devano23",
		"username": "devano23",
		"firstName": "Devon",
		"updatedAt": {
			"offset": -14400,
			"timezone": {
				"name": "-04:00",
				"location": false,
				"transitions": false
			},
			"timestamp": 1601610271
		}
	},
	"likes": 19,
	"links": {
		"html": "https://unsplash.com/photos/N4bE30MecGk",
		"self": "https://api.unsplash.com/photos/N4bE30MecGk",
		"download": "https://unsplash.com/photos/N4bE30MecGk/download",
		"download_location": "https://api.unsplash.com/photos/N4bE30MecGk/download"
	},
	"width": 3456,
	"height": 2304,
	"urlImage": "https://images.unsplash.com/photo-1533212026022-d1affe8cc6dd?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjM0NjQ1fQ",
	"createdAt": {
		"offset": -14400,
		"timezone": {
			"name": "-04:00",
			"location": false,
			"transitions": false
		},
		"timestamp": 1533212106
	},
	"updatedAt": {
		"offset": -14400,
		"timezone": {
			"name": "-04:00",
			"location": false,
			"transitions": false
		},
		"timestamp": 1601064689
	},
	"description": "Desk refresh",
	"altDescription": "turned-on silver iMac beside Apple Magic Mouse"
}
```

{% hint style="info" %}
Based by [UnsplashPhoto](https://git.circleton.com/marstefo/admin-v3/-/blob/master/src/Model/UnsplashPhoto.php) class and [UnsplashUser](https://git.circleton.com/marstefo/admin-v3/-/blob/master/src/Model/UnsplashUser.php) class.
{% endhint %}

### Field **`unsplash_created_at` `(datetime)`**

The creation datetime of the cache unsplash. Used to detect when update the data.

### Field **`nomination` `(string)`**

The user nomination. Values supported:

```text
"Gentile" //Default
"Sua Altezza"
"Sua Eccellenza"
"Sua Eminenza"
"Sua Maestà"
"Sua Santità"
"Chiarissimo"
"Don"
"Dott."
"Magnifico"
"Onorevole"
"Reverendo"
"Illustrissimo"
"Cavaliere"
"Sig."
```

{% hint style="success" %}
Any string can be used and it will work. However, if the user changes his nomination, they will no longer be able to re-enter that string and will only see supported nominations.
{% endhint %}

### Field **`gender` `(string)`**

The gender of the user.

| value | comment |
| :--- | :--- |
| "male" | GENDER\_MALE |
| "female" | GENDER\_FEMALE |

### Field **`quote_id` `(int)`**

The source id of Quote MarStefo quote.

{% hint style="info" %}
To see the project in action: [https://quote.marstefo.ovh](https://quote.marstefo.ovh)
{% endhint %}

### Field **`is_welcome_enabled` `(bool)`**

This option is related to what show in the web manager homepage.

### Field **`is_login_logged_success` `(bool)`**

Whether or not to send a successful login mail notification.

### Field **`is_login_logged_fail` `(bool)`**

Whether or not to send a failed login mail notification.

### Field **`is_disabled_cookies` `(bool)`**

{% hint style="danger" %}
**This field is deprecated and must not be included!**
{% endhint %}

This preference is used to disable the cookie banner code in the web manager.

### Field **`links` `(json)`**

The links to show in the footer of the web manager.  
Example of default content:

```text
[
	{
		"url": "https://admin.marstefo.ovh/profile",
		"name": "Profilo",
		"position": 1
	},
	{
		"url": "https://admin.marstefo.ovh/profile/log",
		"name": "Log accessi",
		"position": 2
	},
	{
		"url": "https://account.marstefo.ovh",
		"name": "Account MarStefo",
		"position": 3
	},
	{
		"url": "https://click.marstefo.ovh",
		"name": "Click MarStefo",
		"position": 4
	},
	{
		"url": "https://crowdesk.dev",
		"name": "Crowdesk",
		"position": 5
	},
	{
		"url": "https://dataset.marstefo.ovh",
		"name": "Dataset MarStefo",
		"position": 6
	},
	{
		"url": "https://bike.marstefo.ovh",
		"name": "Bike MarStefo",
		"position": 7
	},
	{
		"url": "http://wemos.marstefo.ovh",
		"name": "Wemos MarStefo",
		"position": 8
	}
]
```

{% hint style="info" %}
Want to see the Link object?[ See here](https://git.circleton.com/marstefo/admin-v3/-/blob/master/src/Model/Link.php).  
_Based on the_ [_schema_](https://symfony.com/doc/current/_images/components/serializer/serializer_workflow.svg) _on Symfony website, the data was **normalized** then **denormalized** when used to show it._
{% endhint %}

### Field **`telegram_code` `(string)`**

The telegram code verification.

### Field **`telegram_code_created_at` `(datetime)`**

The datetime creation of telegram code verification.

### Field **`telegram_data` `(json)`**

The cache data related to the account telegram.

```text
{
	"id": XXXXXXXX,
	"lastName": "XXXXXX",
	"username": "XXXX",
	"firstName": "XXXX"
}
```

### Field **`fast_lane_token` `(string)`**

{% hint style="danger" %}
**This field is deprecated and must not be included!**
{% endhint %}

The token of FastLane.

{% hint style="info" %}
FastLane is a method of authentication that permit to skip the login process.
{% endhint %}

### Field **`fast_lane_token_created_at` `(datetime)`**

{% hint style="danger" %}
**This field is deprecated and must not be included!**
{% endhint %}

The creation datetime of FastLane token.

### Field **`reset_password_code` `(string)`**

{% hint style="danger" %}
**This field is deprecated and must not be included!**
{% endhint %}

The reset password code used to reset the CircleAdmin password.

### Field **`reset_password_created_at` `(datetime)`**

{% hint style="danger" %}
**This field is deprecated and must not be included!**
{% endhint %}

The creation datetime of the reset password code,

### Field **`is_allowed_to_disable_servers` `(bool)`**

Enable the possibility to block the servers if the user has payments not payed.

{% hint style="warning" %}
This value is not used because the Proxmox firewall does not work well.
{% endhint %}

### Field **`limit_refresh` `(int)`**

The limit refresh is the number of tokens that can be used to sync immediately the servers status. This value is resetted every hour.

{% hint style="info" %}
By default this value is setted as LIMIT\_REFRESH\_DEFAULT = 10.
{% endhint %}

### Field **`limit_refresh_created_at` `(datetime)`**

The creation datetime  of the limit refresh.

### Field **`competency` `(string)`**

The competency of the user. Is also used in circleton.com .

### Field **`website` `(string)`**

The personal website of the user. Is also used in circleton.com .

### Field **`is_preferring_url_short` `(bool)`**

Activate or deactivate the automatic link generation of Click MarStefo. Used in Project.

{% hint style="info" %}
To see more: [http://click.marstefo.ovh](http://click.marstefo.ovh)
{% endhint %}

## Updates

{% hint style="info" %}
Fields can grow, but basic functionality has already been implemented. 😊
{% endhint %}

