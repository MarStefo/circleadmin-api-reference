---
description: >-
  The Telegram integration add the possibility to sync the photo profile and
  skip the sms code in the initial wizard.
---

# Telegram

At the moment, the Telegram integration allow to sync the photo profile \(if there are at least one photo profile and it is public\). Also it can be used to skip the sms code check if the form is submitted with blank value.

## Command supported by the MarStefoAdminBot

{% hint style="warning" %}
The name of the bot can be changed \(and most likely it will\).
{% endhint %}

| command | comment |
| :--- | :--- |
| /start | Also used as test command to check if bot is alive |
| /otp | Can be used to bypass the sms code check in the initial wizard |
| /connetti \(\[0-9\]{5}\) | Can be used to connect the telegram account into CircleAdmin |
| /balance | Can be used to get the current balance |



