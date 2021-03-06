---
title: auth.exportAuthorization
description: Returns data for copying authorization to another data-centre.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/auth_exportAuthorization.html
---
# Method: auth.exportAuthorization
[Back to methods index](index.md)



Returns data for copying authorization to another data-centre.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|dc\_id|[int](../types/int.md) | Number of a target data-centre | Yes|


### Return type: [auth.ExportedAuthorization](../types/auth.ExportedAuthorization.md)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$auth_ExportedAuthorization = $MadelineProto->auth->exportAuthorization(['dc_id' => int, ]);
```

Or, if you're into Lua:

```lua
auth_ExportedAuthorization = auth.exportAuthorization({dc_id=int, })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|DC_ID_INVALID|The provided DC ID is invalid|


