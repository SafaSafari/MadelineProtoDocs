---
title: importedContact
description: Successfully imported contact.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: importedContact  
[Back to constructors index](index.md)



Successfully imported contact.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|user\_id|[int](../types/int.md) | Yes|User identifier|
|client\_id|[long](../types/long.md) | Yes|The contact's client identifier (passed to one of the [InputContact](../types/InputContact.md) constructors)|



### Type: [ImportedContact](../types/ImportedContact.md)


### Example:

```php
$importedContact = ['_' => 'importedContact', 'user_id' => int, 'client_id' => long];
```  


Or, if you're into Lua:

```lua
importedContact={_='importedContact', user_id=int, client_id=long}

```


