---
title: secureSecretSettings
description: Secure settings
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: secureSecretSettings  
[Back to constructors index](index.md)



Secure settings

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|secure\_algo|[SecurePasswordKdfAlgo](../types/SecurePasswordKdfAlgo.md) | Yes|Secure KDF algo|
|secure\_secret|[bytes](../types/bytes.md) | Yes|Secure secret|
|secure\_secret\_id|[long](../types/long.md) | Yes|Secret ID|



### Type: [SecureSecretSettings](../types/SecureSecretSettings.md)


### Example:

```php
$secureSecretSettings = ['_' => 'secureSecretSettings', 'secure_algo' => SecurePasswordKdfAlgo, 'secure_secret' => 'bytes', 'secure_secret_id' => long];
```  


Or, if you're into Lua:

```lua
secureSecretSettings={_='secureSecretSettings', secure_algo=SecurePasswordKdfAlgo, secure_secret='bytes', secure_secret_id=long}

```


