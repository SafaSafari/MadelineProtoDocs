---
title: messages.receivedMessages
description: Confirms receipt of messages by a client, cancels PUSH-notification sending.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: messages.receivedMessages  
[Back to methods index](index.md)


Confirms receipt of messages by a client, cancels PUSH-notification sending.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|max\_id|[int](../types/int.md) | Maximum message ID available in a client. | Yes|


### Return type: [Vector\_of\_int](../types/int.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Vector_of_int = $MadelineProto->messages->receivedMessages(['max_id' => int, ]);
```

Or, if you're into Lua:

```lua
Vector_of_int = messages.receivedMessages({max_id=int, })
```
