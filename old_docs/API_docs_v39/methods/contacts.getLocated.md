---
title: contacts.getLocated
description: Get contacts near you
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/contacts_getLocated.html
---
# Method: contacts.getLocated
[Back to methods index](index.md)



Get contacts near you

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|background|[Bool](../types/Bool.md) | While the geolocation of the current user is public, clients should update it in the background every half-an-hour or so, while setting this flag. <br>Do this only if the new location is more than 1 KM away from the previous one, or if the previous location is unknown. | Optional|
|geo\_point|[InputGeoPoint](../types/InputGeoPoint.md) | Geolocation | Optional|
|self\_expires|[int](../types/int.md) | If set, the geolocation of the current user will be public for the specified number of seconds; pass 0x7fffffff to disable expiry, 0 to make the current geolocation private; if the flag isn't set, no changes will be applied. | Optional|


### Return type: [Updates](../types/Updates.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Updates = $MadelineProto->contacts->getLocated(['background' => Bool, 'geo_point' => InputGeoPoint, 'self_expires' => int, ]);
```

Or, if you're into Lua:

```lua
Updates = contacts.getLocated({background=Bool, geo_point=InputGeoPoint, self_expires=int, })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|GEO_POINT_INVALID|Invalid geoposition provided|
|406|USERPIC_UPLOAD_REQUIRED|You must have a profile picture to publish your geolocation|


