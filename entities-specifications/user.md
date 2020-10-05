---
description: Specifications for the User table
---

# User

## Field **`id` `(int)`**

The identifier of the user.

## Field **`email` `(string)`**

The email of the user.

## Field **`roles` `(json)`**

The roles of the user. For more information read the Roles page.





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

{% hint style="warning" %}
 **DC2Type** is the proprietary format of Symfony PHP framework. Will be updated to classic format \(eg. JSON\) soon!
{% endhint %}

{% hint style="info" %}

{% endhint %}



