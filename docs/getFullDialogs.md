---
title: getFullDialogs
description: getFullDialogs parameters, return type and example
redirect_from: /get_full_dialogs.html
---
## Method: getDialogs  

Gets full list of dialogs

### Return type: Array of [Dialog objects](API_docs/types/Dialog.md)

### Example ([now fully async!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
$Dialogs = yield $MadelineProto->getFullDialogs();
```

Or, if you're into Lua:

```lua
Dialogs = getFullDialogs()
```

