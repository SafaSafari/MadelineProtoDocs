---
title: messages.getPeerSettings
description: Get peer settings
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getPeerSettings.html
---
# Method: messages.getPeerSettings
[Back to methods index](index.md)



Get peer settings

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](../types/InputPeer.md) | The peer | Optional|


### Return type: [PeerSettings](../types/PeerSettings.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$PeerSettings = $MadelineProto->messages->getPeerSettings(['peer' => InputPeer, ]);
```

Or, if you're into Lua:

```lua
PeerSettings = messages.getPeerSettings({peer=InputPeer, })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|CHANNEL_INVALID|The provided channel is invalid|
|400|PEER_ID_INVALID|The provided peer id is invalid|


