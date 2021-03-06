---
title: help.recentMeUrls
description: Recent t.me URLs
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/constructors/help_recentMeUrls.html
---
# Constructor: help.recentMeUrls  
[Back to constructors index](index.md)



Recent t.me URLs

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|urls|Array of [RecentMeUrl](../types/RecentMeUrl.md) | Yes|URLs|
|chats|Array of [Chat](../types/Chat.md) | Yes|Chats|
|users|Array of [User](../types/User.md) | Yes|Users|



### Type: [help.RecentMeUrls](../types/help.RecentMeUrls.md)


### Example:

```php
$help_recentMeUrls = ['_' => 'help.recentMeUrls', 'urls' => [RecentMeUrl, RecentMeUrl], 'chats' => [Chat, Chat], 'users' => [User, User]];
```  


Or, if you're into Lua:

```lua
help_recentMeUrls={_='help.recentMeUrls', urls={RecentMeUrl}, chats={Chat}, users={User}}

```


