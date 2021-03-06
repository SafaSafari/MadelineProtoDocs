---
title: messageEntityMentionName
description: Message entity representing a [user mention](https://t.me/test): for *creating* a mention use [inputMessageEntityMentionName](../constructors/inputMessageEntityMentionName.md).
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: messageEntityMentionName  
[Back to constructors index](index.md)



Message entity representing a [user mention](https://t.me/test): for *creating* a mention use [inputMessageEntityMentionName](../constructors/inputMessageEntityMentionName.md).

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|offset|[int](../types/int.md) | Yes|Offset of message entity within message (in UTF-8 codepoints)|
|length|[int](../types/int.md) | Yes|Length of message entity within message (in UTF-8 codepoints)|
|user\_id|[int](../types/int.md) | Yes|Identifier of the user that was mentioned|



### Type: [MessageEntity](../types/MessageEntity.md)


### Example:

```php
$messageEntityMentionName = ['_' => 'messageEntityMentionName', 'offset' => int, 'length' => int, 'user_id' => int];
```  


Or, if you're into Lua:

```lua
messageEntityMentionName={_='messageEntityMentionName', offset=int, length=int, user_id=int}

```


