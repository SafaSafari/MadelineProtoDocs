---
title: account.saveWallPaper
description: Install/uninstall wallpaper
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_saveWallPaper.html
---
# Method: account.saveWallPaper  
[Back to methods index](index.md)


Install/uninstall wallpaper

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|wallpaper|[InputWallPaper](../types/InputWallPaper.md) | Wallpaper to save | Yes|
|unsave|[Bool](../types/Bool.md) | Uninstall wallpaper? | Yes|
|settings|[WallPaperSettings](../types/WallPaperSettings.md) | Wallpaper settings | Yes|


### Return type: [Bool](../types/Bool.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Bool = $MadelineProto->account->saveWallPaper(['wallpaper' => InputWallPaper, 'unsave' => Bool, 'settings' => WallPaperSettings, ]);
```

Or, if you're into Lua:

```lua
Bool = account.saveWallPaper({wallpaper=InputWallPaper, unsave=Bool, settings=WallPaperSettings, })
```

