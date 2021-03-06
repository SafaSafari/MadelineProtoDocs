---
title: messages.updateDialogFiltersOrder
description: Reorder [folders](https://core.telegram.org/api/folders)
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_updateDialogFiltersOrder.html
---
# Method: messages.updateDialogFiltersOrder
[Back to methods index](index.md)



Reorder [folders](https://core.telegram.org/api/folders)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|order|Array of [int](../types/int.md) | New [folder](https://core.telegram.org/api/folders) order | Yes|


### Return type: [Bool](../types/Bool.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Bool = $MadelineProto->messages->updateDialogFiltersOrder(['order' => [int, int], ]);
```

Or, if you're into Lua:

```lua
Bool = messages.updateDialogFiltersOrder({order={int}, })
```

