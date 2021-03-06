---
title: account.setPrivacy
description: Change privacy settings of current account
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_setPrivacy.html
---
# Method: account.setPrivacy
[Back to methods index](index.md)



Change privacy settings of current account

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|key|[InputPrivacyKey](../types/InputPrivacyKey.md) | Peers to which the privacy rules apply | Yes|
|rules|Array of [InputPrivacyRule](../types/InputPrivacyRule.md) | New privacy rules | Yes|


### Return type: [account.PrivacyRules](../types/account.PrivacyRules.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$account_PrivacyRules = $MadelineProto->account->setPrivacy(['key' => InputPrivacyKey, 'rules' => [InputPrivacyRule, InputPrivacyRule], ]);
```

Or, if you're into Lua:

```lua
account_PrivacyRules = account.setPrivacy({key=InputPrivacyKey, rules={InputPrivacyRule}, })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|PRIVACY_KEY_INVALID|The privacy key is invalid|
|400|PRIVACY_VALUE_INVALID|The specified privacy rule combination is invalid|
|401|SESSION_PASSWORD_NEEDED|2FA is enabled, use a password to login|


