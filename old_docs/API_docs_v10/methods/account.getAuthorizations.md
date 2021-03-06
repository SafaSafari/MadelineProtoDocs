---
title: account.getAuthorizations
description: Get logged-in sessions
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_getAuthorizations.html
---
# Method: account.getAuthorizations
[Back to methods index](index.md)



Get logged-in sessions



### Return type: [account.Authorizations](../types/account.Authorizations.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$account_Authorizations = $MadelineProto->account->getAuthorizations();
```

Or, if you're into Lua:

```lua
account_Authorizations = account.getAuthorizations({})
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|406|AUTH_KEY_DUPLICATED|An auth key with the same ID was already generated|
|401|SESSION_PASSWORD_NEEDED|2FA is enabled, use a password to login|


