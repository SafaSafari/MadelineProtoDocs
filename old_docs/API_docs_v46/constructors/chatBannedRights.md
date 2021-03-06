---
title: chatBannedRights
description: Represents the rights of a normal user in a [supergroup/channel/chat](https://core.telegram.org/api/channel). In this case, the flags are inverted: if set, a flag **does not allow** a user to do X.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: chatBannedRights  
[Back to constructors index](index.md)



Represents the rights of a normal user in a [supergroup/channel/chat](https://core.telegram.org/api/channel). In this case, the flags are inverted: if set, a flag **does not allow** a user to do X.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|view\_messages|[Bool](../types/Bool.md) | Optional|If set, does not allow a user to view messages in a [supergroup/channel/chat](https://core.telegram.org/api/channel)|
|send\_messages|[Bool](../types/Bool.md) | Optional|If set, does not allow a user to send messages in a [supergroup/chat](https://core.telegram.org/api/channel)|
|send\_media|[Bool](../types/Bool.md) | Optional|If set, does not allow a user to send any media in a [supergroup/chat](https://core.telegram.org/api/channel)|
|send\_stickers|[Bool](../types/Bool.md) | Optional|If set, does not allow a user to send stickers in a [supergroup/chat](https://core.telegram.org/api/channel)|
|send\_gifs|[Bool](../types/Bool.md) | Optional|If set, does not allow a user to send gifs in a [supergroup/chat](https://core.telegram.org/api/channel)|
|send\_games|[Bool](../types/Bool.md) | Optional|If set, does not allow a user to send games in a [supergroup/chat](https://core.telegram.org/api/channel)|
|send\_inline|[Bool](../types/Bool.md) | Optional|If set, does not allow a user to use inline bots in a [supergroup/chat](https://core.telegram.org/api/channel)|
|embed\_links|[Bool](../types/Bool.md) | Optional|If set, does not allow a user to embed links in the messages of a [supergroup/chat](https://core.telegram.org/api/channel)|
|send\_polls|[Bool](../types/Bool.md) | Optional|If set, does not allow a user to send stickers in a [supergroup/chat](https://core.telegram.org/api/channel)|
|change\_info|[Bool](../types/Bool.md) | Optional|If set, does not allow any user to change the description of a [supergroup/chat](https://core.telegram.org/api/channel)|
|invite\_users|[Bool](../types/Bool.md) | Optional|If set, does not allow any user to invite users in a [supergroup/chat](https://core.telegram.org/api/channel)|
|pin\_messages|[Bool](../types/Bool.md) | Optional|If set, does not allow any user to pin messages in a [supergroup/chat](https://core.telegram.org/api/channel)|
|until\_date|[int](../types/int.md) | Yes|Validity of said permissions (it is considered forever any value less then 30 seconds or more then 366 days).|



### Type: [ChatBannedRights](../types/ChatBannedRights.md)


### Example:

```php
$chatBannedRights = ['_' => 'chatBannedRights', 'view_messages' => Bool, 'send_messages' => Bool, 'send_media' => Bool, 'send_stickers' => Bool, 'send_gifs' => Bool, 'send_games' => Bool, 'send_inline' => Bool, 'embed_links' => Bool, 'send_polls' => Bool, 'change_info' => Bool, 'invite_users' => Bool, 'pin_messages' => Bool, 'until_date' => int];
```  


Or, if you're into Lua:

```lua
chatBannedRights={_='chatBannedRights', view_messages=Bool, send_messages=Bool, send_media=Bool, send_stickers=Bool, send_gifs=Bool, send_games=Bool, send_inline=Bool, embed_links=Bool, send_polls=Bool, change_info=Bool, invite_users=Bool, pin_messages=Bool, until_date=int}

```


