---
title: phoneCallWaiting
description: Incoming phone call
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: phoneCallWaiting  
[Back to constructors index](index.md)



Incoming phone call

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|id|[long](../types/long.md) | Yes|Call ID|
|access\_hash|[long](../types/long.md) | Yes|Access hash|
|date|[int](../types/int.md) | Yes|Date|
|admin\_id|[int](../types/int.md) | Yes|Admin ID|
|participant\_id|[int](../types/int.md) | Yes|Participant ID|
|protocol|[PhoneCallProtocol](../types/PhoneCallProtocol.md) | Yes|Phone call protocol info|
|receive\_date|[int](../types/int.md) | Optional|When was the phone call received|



### Type: [PhoneCall](../types/PhoneCall.md)


### Example:

```php
$phoneCallWaiting = ['_' => 'phoneCallWaiting', 'id' => long, 'access_hash' => long, 'date' => int, 'admin_id' => int, 'participant_id' => int, 'protocol' => PhoneCallProtocol, 'receive_date' => int];
```  


Or, if you're into Lua:

```lua
phoneCallWaiting={_='phoneCallWaiting', id=long, access_hash=long, date=int, admin_id=int, participant_id=int, protocol=PhoneCallProtocol, receive_date=int}

```


