---
description: Specifications for the User table
---

# User

## Summary

| **field** | **type** |
| :--- | :--- |
| id | int |
| email | string |
| roles | json |
| password | string |
| name | string |
| surname | string |
| birthday | date |
| phone | string |
| address | text |
| image | string |
| is\_deleted | bool |
| credit | int |
| wizard\_status | int |
| phone\_verify | string |
| notification\_type | int |
| created\_at | datetime |
| unsplash\_query | string |
| unsplash\_photo | DC2Type:object |
| unsplash\_created\_at | datetime |
| nomination | string |
| gender | string |
| quote\_id | int |
| is\_welcome\_enabled | bool |
| is\_login\_logged\_success | bool |
| is\_login\_logged\_fail | bool |
| is\_disabled\_cookies | bool |
| links | DC2Type:array |
| telegram\_code | string |
| telegram\_code\_created\_at | datetime |
| telegram\_data | DC2Type:array |
| fast\_lane\_token | string |
| fast\_lane\_token\_created\_at | datetime |
| reset\_password\_code | string |
| reset\_password\_created\_at | datetime |
| is\_allowed\_to\_disable\_servers | bool |
| limit\_refresh | int |
| limit\_refresh\_created\_at | datetime |
| competency | text |
| website | text |
| is\_preferring\_url\_short | bool |

### Field **`id` `(int)`**

The identifier of the user.

### Field **`email` `(string)`**

The email of the user.

### Field **`roles` `(json)`**

The roles of the user. For more information read the Roles page.

{% page-ref page="../extra/roles.md" %}

### Field **`password` `(string)`**

The password of the user in a Symfony format \(using encoder _Symfony\Component\Security\Core\Encoder\MigratingPasswordEncoder_\), [read more](https://symfony.com/doc/current/security.html#c-encoding-passwords).

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
All monetary values are multiplied by 100. To restore the original value, simply divide by 100. 🧐
{% endhint %}

### Field **`wizard_status` `(int)`**

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

### Field **`unsplash_photo` `(DC2Type:object)`**

The rapresentation of a object that contains the photo cache. This value is resetted every night at 00.00.

{% hint style="warning" %}
 **DC2Type** is the proprietary format of Symfony PHP framework. Will be updated to classic format \(eg. JSON\) soon!
{% endhint %}

### Field **`unsplash_created_at` `(datetime)`**

The creation datetime of the cache unsplash. Used to detect when update the data.

### Field **`nomination` `(string)`**

The user nomination. Values supported:

```text
"Gentile"
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
| "Maschio" | GENDER\_MALE |
| "Femmina" | GENDER\_FEMALE |

{% hint style="warning" %}
TODO: The values will be translated to English soon.
{% endhint %}

### Field **`quote_id` `(int)`**

The id of Quote MarStefo quote.

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

This preference is used to disable the cookie banner code in the web manager.

### Field **`links` `(DC2Type:array)`**

The link to show in the footer of the web manager.

{% hint style="warning" %}
 **DC2Type** is the proprietary format of Symfony PHP framework. Will be updated to classic format \(eg. JSON\) soon!
{% endhint %}

### Field **`telegram_code` `(string)`**

The telegram code verification.

### Field **`telegram_code_created_at` `(datetime)`**

The datetime creation of telegram code verification.

### Field **`telegram_data` `(DC2Type:array)`**

The cache data related to the account telegram.

{% hint style="warning" %}
 **DC2Type** is the proprietary format of Symfony PHP framework. Will be updated to classic format \(eg. JSON\) soon!
{% endhint %}

### Field **`fast_lane_token` `(string)`**

The token of FastLane.

{% hint style="info" %}
FastLane is a method of authentication that permit to skip the login process.
{% endhint %}

### Field **`fast_lane_token_created_at` `(datetime)`**

The creation datetime of FastLane token.

### Field **`reset_password_code` `(string)`**

The reset password code used to reset the CircleAdmin password.

### Field **`reset_password_created_at` `(datetime)`**

The creation datetime of the reset password code,

### Field **`is_allowed_to_disable_servers` `(bool)`**

Enable the possibility to block the servers if the user has payments not payed.

{% hint style="warning" %}
This value is not used because the Proxmox firewall does not work well.
{% endhint %}

### Field **`limit_refresh` `(int)`**

The limit refresh is the number of tokens that can be used to sync immediately the servers status. This value is resetted every hour.

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

