---
description: CircleAdmin use the power of roles of Symfony.
---

# Roles

## Symfony Roles

All roles must start with "ROLE\_" and may have a hierarchy.   
For instance, an user with administrative roles will contains this json:

```text
[
	"ROLE_ADMIN",
	"ROLE_USER",
	"ROLE_SUPER_ADMIN"
]
```

{% hint style="info" %}
For more informations about Symfony roles read: [https://symfony.com/doc/current/security.html\#roles](https://symfony.com/doc/current/security.html#roles)
{% endhint %}

## Main roles

The Main roles defines the phisical group of an user.

* '**ROLE\_USER**': "User with basic applications", 
* '**ROLE\_BASE**': "User with main applications", 
* '**ROLE\_SERVER**': "User with one or more servers assigned", 
* '**ROLE\_CIRCLETON**': "User belonging to the CircleTon group", 
* '**ROLE\_ADMIN**': "Administrator user", 
* '**ROLE\_SUPER\_ADMIN**': "Administrator user with impersonation ability".

## Functional roles

The Functional roles defines the access of an application.

* '**ROLE\_PROPOSAL**': "Access to the Proposals application", 
* '**ROLE\_COMMUNICATION**': "Access to the Communications application", 
* '**ROLE\_PROJECT**': "Access to the Projects application", 
* '**ROLE\_BALANCE**': "Access to the Budget application", 
* '**ROLE\_MEETING**': "Access to the Meeting application", 
* '**ROLE\_CATALOG**': "Access to the Catalog application", 
* '**ROLE\_SERVER\_MANAGER**': "Access to the Server application".

{% page-ref page="applications.md" %}



## Hierarchy

```text
role_hierarchy:
    ROLE_USER:        [ROLE_COMMUNICATION]
    ROLE_BASE:        [ROLE_USER,ROLE_PROPOSAL,ROLE_PROJECT]
    ROLE_SERVER:      [ROLE_BASE,ROLE_SERVER_MANAGER,ROLE_BALANCE,ROLE_CATALOG]
    ROLE_CIRCLETON:   [ROLE_BASE,ROLE_MEETING]
    ROLE_ADMIN:       [ROLE_CIRCLETON,ROLE_SERVER]
    ROLE_SUPER_ADMIN: [ROLE_ADMIN, ROLE_ALLOWED_TO_SWITCH]
```

{% hint style="info" %}
For example, **ROLE\_BASE** inherit ROLE\_USER, ROLE\_PROPOSAL and ROLE\_PROJECT. Moreover, ROLE\_USER inherit ROLE\_COMMUNICATION.
{% endhint %}



