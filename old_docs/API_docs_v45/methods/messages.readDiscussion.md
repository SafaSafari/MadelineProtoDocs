---
title: messages.readDiscussion
description: messages.readDiscussion parameters, return type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_readDiscussion.html
---
# Method: messages.readDiscussion
[Back to methods index](index.md)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](../types/InputPeer.md) | Optional|
|msg\_id|[int](../types/int.md) | Yes|
|read\_max\_id|[int](../types/int.md) | Yes|


### Return type: [Bool](../types/Bool.md)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Bool = $MadelineProto->messages->readDiscussion(['peer' => InputPeer, 'msg_id' => int, 'read_max_id' => int, ]);
```

Or, if you're into Lua:

```lua
Bool = messages.readDiscussion({peer=InputPeer, msg_id=int, read_max_id=int, })
```

