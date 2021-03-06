---
title: keyboardButtonCallback
description: Callback button
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: keyboardButtonCallback  
[Back to constructors index](index.md)



Callback button

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|text|[string](../types/string.md) | Yes|Button text|
|data|[bytes](../types/bytes.md) | Yes|Callback data|



### Type: [KeyboardButton](../types/KeyboardButton.md)


### Example:

```php
$keyboardButtonCallback = ['_' => 'keyboardButtonCallback', 'text' => 'string', 'data' => 'bytes'];
```  


Or, if you're into Lua:

```lua
keyboardButtonCallback={_='keyboardButtonCallback', text='string', data='bytes'}

```


