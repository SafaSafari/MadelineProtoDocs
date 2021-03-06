---
title: danog\MadelineProto\MTProto: Manages all of the mtproto stuff.
description: 

image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# `danog\MadelineProto\MTProto`
[Back to index](../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Manages all of the mtproto stuff.  




## Constants
* `danog\MadelineProto\MTProto::RELEASE`: Release version.

* `danog\MadelineProto\MTProto::NOT_LOGGED_IN`: We're not logged in.

* `danog\MadelineProto\MTProto::WAITING_CODE`: We're waiting for the login code.

* `danog\MadelineProto\MTProto::WAITING_SIGNUP`: We're waiting for parameters to sign up.

* `danog\MadelineProto\MTProto::WAITING_PASSWORD`: We're waiting for the 2FA password.

* `danog\MadelineProto\MTProto::LOGGED_IN`: We're logged in.

* `danog\MadelineProto\MTProto::SECRET_EMPTY`: Secret chat was not found.

* `danog\MadelineProto\MTProto::SECRET_REQUESTED`: Secret chat was requested.

* `danog\MadelineProto\MTProto::SECRET_READY`: Secret chat was found.


## Method list:
* `serializeSession(): \Generator`
* `serializeAll(): void`
* `cleanup(): \Generator`
* `logger(string $param, int $level, string $file): void`
* `getMethodNamespaces(): array`
* `getMethodsNamespaced(): array`
* `getTL(): \danog\MadelineProto\TL\TL`
* `getLogger()`
* `getPsrLogger()`
* `getHTTPClient(): \Amp\Http\Client\HttpClient`
* `getDNSClient(): \Amp\Dns\Resolver`
* `fileGetContents(string $url): \Generator`
* `getDataCenterConnections(): \danog\MadelineProto\DataCenterConnection[]`
* `getDataCenterId(): int|string`
* `isIpc(): bool`
* `updateSettings(\danog\MadelineProto\SettingsAbstract $settings): \Generator`
* `getSettings(): \danog\MadelineProto\Settings`
* `setupLogger(): void`
* `hasAllAuth(): bool`
* `connectToAllDcs(bool $reconnectAll): \Generator`
* `resetUpdateState(): void`
* `getCdnConfig(string $datacenter): \Generator`
* `getCachedConfig(): array`
* `getConfig(array $config, array $options): \Generator`
* `getSelf(): array|bool`
* `fullGetSelf(): \Generator<array|bool>`
* `getAuthorization(): int`
* `getHint(): string`
* `hasReportPeers(): bool`
* `setReportPeers(int|string $userOrId): \Generator`
* `report(string $message, string $parseMode): \Generator`
* `getAllMethods(): array`
* `getMethodCallbacks(): array`
* `getMethodBeforeCallbacks(): array`
* `getConstructorCallbacks(): array`
* `getConstructorBeforeCallbacks(): array`
* `getConstructorSerializeCallbacks(): array`
* `getTypeMismatchCallbacks(): array`
* `init(): void`
* `initAsynchronously(): \Generator`
* `inited(): bool`
* `forceInit(bool $inited): void`
* `methodCall(string $method, array|\Generator $args, array $aargs): mixed`
* `methodCallAsyncRead(string $method, array|\Generator $args, array $aargs): \Generator`
* `methodCallAsyncWrite(string $method, array|\Generator $args, array $aargs): \Generator`
* `toSupergroup(int $id): float|int`
* `fromSupergroup(int $id): float|int`
* `isSupergroup(int $id): bool`
* `addUser(array $user): \Generator`
* `peerIsset(mixed $id): \Generator`
* `getFolderId(mixed $id): ?int`
* `getId(mixed $id): int`
* `getInfo(mixed $id, bool $recursive): \Generator Info object`
* `fullChatLastUpdated(mixed $id): \Generator<int>`
* `getFullInfo(mixed $id): \Generator FullInfo object`
* `getPwrChat(mixed $id): \Generator<array> Chat object`
* `resolveUsername(string $username): \Generator`
* `uploadFromUrl(string|\danog\MadelineProto\FileCallbackInterface $url, int $size, string $fileName, callable $cb, bool $encrypted): \Generator`
* `uploadFromCallable(mixed $callable, int $size, string $mime, string $fileName, callable $cb, bool $seekable, bool $encrypted): \Generator`
* `uploadFromTgfile(mixed $media, callable $cb, bool $encrypted): \Generator`
* `getFileInfo(mixed $constructor): \Generator<array>`
* `getPropicInfo(mixed $messageMedia): \Generator<array>`
* `extractBotAPIFile(array $info): ?array`
* `getDownloadInfo(mixed $messageMedia): \Generator<array>`
* `downloadToDir(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $dir, callable $cb): \Generator`
* `downloadToFile(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $file, callable $cb): \Generator Downloaded file path`
* `downloadToCallable(mixed $messageMedia, callable|\danog\MadelineProto\FileCallbackInterface $callable, callable $cb, bool $seekable, int $offset, int $end, int $part_size): \Generator`
* `downloadToBrowser(array|string $messageMedia, callable $cb): \Generator`
* `downloadToStream(mixed $messageMedia, mixed|\danog\MadelineProto\FileCallbackInterface $stream, callable $cb, int $offset, int $end): \Generator`
* `downloadToResponse(array|string $messageMedia, \ServerRequest $request, callable $cb): \Generator Returned response`
* `uploadEncrypted(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb): \Generator`
* `upload(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb, bool $encrypted): \Generator`
* `uploadFromStream(mixed $stream, int $size, string $mime, string $fileName, callable $cb, bool $encrypted): \Generator`
* `acceptSecretChat(array $params): \Generator`
* `requestSecretChat(mixed $user): \Generator`
* `rekey(int $chat): \Generator`
* `secretChatStatus(int $chat): \int One of MTProto::SECRET_EMPTY, MTProto::SECRET_REQUESTED, MTProto::SECRET_READY`
* `getSecretChat(array|int $chat): array`
* `hasSecretChat(array|int $chat): bool`
* `discardSecretChat(int $chat): \Generator`
* `mbStrlen(string $text): float|int`
* `mbSubstr(string $text, int $offset, ?int $length): string`
* `mbStrSplit(string $text, int $length): array`
* `MTProtoToBotAPI(array $data): \Generator<array>`
* `botAPIToMTProto(array $arguments): \Generator<array>`
* `unpackFileId(string $fileId): \array Unpacked file ID`
* `tdcliToTd(array $params, array $key): array`
* `tdToMTProto(array $params): \Generator<array>`
* `MTProtoToTdcli(mixed $params): \Generator`
* `MTProtoToTd(mixed $params): \Generator`
* `tdToTdcli(mixed $params): mixed`
* `requestCall(mixed $user): \Generator`
* `acceptCall(array $call): \Generator`
* `confirmCall(array $params): \Generator`
* `completeCall(array $params): \Generator`
* `callStatus(int $id): int`
* `getCall(int $call): array`
* `discardCall(array $call, array $reason, array $rating, bool $need_debug): \Generator`
* `getDialogs(bool $force): \Generator`
* `getFullDialogs(bool $force): \Generator`
* `setEventHandler(class-string<\danog\MadelineProto\EventHandler> $eventHandler): \Generator`
* `unsetEventHandler(bool $disableUpdateHandling): void`
* `getEventHandler(): \danog\MadelineProto\EventHandler`
* `hasEventHandler(): bool`
* `setWebhook(string $hook_url, string $pem_path): void`
* `setCallback(callable $callback): void`
* `logout(): \Generator`
* `botLogin(string $token): \Generator`
* `phoneLogin(string $number, int $sms_type): \Generator`
* `completePhoneLogin(string $code): \Generator`
* `importAuthorization(mixed $authorization): \Generator`
* `exportAuthorization(): \Generator`
* `completeSignup(string $first_name, string $last_name): \Generator`
* `complete2faLogin(string $password): \Generator`
* `update2fa(array $params): \Generator`
* `initSelfRestart(): void`
* `loop(callable|null $callback): \Generator`
* `stop(): void`
* `restart(): void`
* `loopFork(): \Amp\Promise`
* `closeConnection(string $message): void`
* `setNoop(): void`
* `start(): \Generator`
* `getWebTemplate(): string`
* `setWebTemplate(string $template): void`
* `checkTos(): \Generator`
* `acceptTos(): \Generator`
* `declineTos(): \Generator`

## Methods:
### `serializeSession(): \Generator`

Serialize session, returning object to serialize to db.


#### See also: 
* `\Generator`




### `serializeAll(): void`

Serialize all instances.
CALLED ONLY ON SHUTDOWN.


### `cleanup(): \Generator`

Cleanup memory and session file.


#### See also: 
* `\Generator`




### `logger(string $param, int $level, string $file): void`

Logger.


Parameters:
* `$param`: `string` Parameter  
* `$level`: `int` Logging level  
* `$file`: `string` File where the message originated  



### `getMethodNamespaces(): array`

Get TL namespaces.



### `getMethodsNamespaced(): array`

Get namespaced methods (method => namespace).



### `getTL(): \danog\MadelineProto\TL\TL`

Get TL serializer.


#### See also: 
* `\danog\MadelineProto\TL\TL`




### `getLogger()`

Get logger.



### `getPsrLogger()`

Get PSR logger.



### `getHTTPClient(): \Amp\Http\Client\HttpClient`

Get async HTTP client.


#### See also: 
* `\Amp\Http\Client\HttpClient`




### `getDNSClient(): \Amp\Dns\Resolver`

Get async DNS client.


#### See also: 
* `\Amp\Dns\Resolver`




### `fileGetContents(string $url): \Generator`

Get contents of remote file asynchronously.


Parameters:
* `$url`: `string` URL  


Fully typed return value:
```
\Generator<int, \Amp\Promise<string>, mixed, string>
```
#### See also: 
* `\Amp\Promise`
* `\Generator`




### `getDataCenterConnections(): \danog\MadelineProto\DataCenterConnection[]`

Get all datacenter connections.


#### See also: 
* `\danog\MadelineProto\DataCenterConnection`




### `getDataCenterId(): int|string`

Get main DC ID.



### `isIpc(): bool`

Whether we're an IPC client instance.



### `updateSettings(\danog\MadelineProto\SettingsAbstract $settings): \Generator`

Parse, update and store settings.


Parameters:
* `$settings`: `\danog\MadelineProto\SettingsAbstract` Settings  


#### See also: 
* `\danog\MadelineProto\SettingsAbstract`
* `\Generator`




### `getSettings(): \danog\MadelineProto\Settings`

Return current settings.


#### See also: 
* [`\danog\MadelineProto\Settings`: Settings class used for configuring MadelineProto.](./Settings.md)




### `setupLogger(): void`

Setup logger.



### `hasAllAuth(): bool`

Checks whether all datacenters are authorized.



### `connectToAllDcs(bool $reconnectAll): \Generator`

Connects to all datacenters and if necessary creates authorization keys, binds them and writes client info.


Parameters:
* `$reconnectAll`: `bool` Whether to reconnect to all DCs  


#### See also: 
* `\Generator`




### `resetUpdateState(): void`

Reset the update state and fetch all updates from the beginning.



### `getCdnConfig(string $datacenter): \Generator`

Store RSA keys for CDN datacenters.


Parameters:
* `$datacenter`: `string` DC ID  


#### See also: 
* `\Generator`




### `getCachedConfig(): array`

Get cached server-side config.



### `getConfig(array $config, array $options): \Generator`

Get cached (or eventually re-fetch) server-side config.


Parameters:
* `$config`: `array` Current config  
* `$options`: `array` Options for method call  


#### See also: 
* `\Generator`




### `getSelf(): array|bool`

Get info about the logged-in user, cached.



### `fullGetSelf(): \Generator<array|bool>`

Get info about the logged-in user, not cached.


#### See also: 
* `\Generator`




### `getAuthorization(): int`

Get authorization info.



### `getHint(): string`

Get current password hint.



### `hasReportPeers(): bool`

Check if has report peers.



### `setReportPeers(int|string $userOrId): \Generator`

Set peer(s) where to send errors occurred in the event loop.


Parameters:
* `$userOrId`: `int|string` Username(s) or peer ID(s)  


#### See also: 
* `\Generator`




### `report(string $message, string $parseMode): \Generator`

Report an error to the previously set peer.


Parameters:
* `$message`: `string` Error to report  
* `$parseMode`: `string` Parse mode  


#### See also: 
* `\Generator`




### `getAllMethods(): array`

Get full list of MTProto and API methods.



### `getMethodCallbacks(): array`

Called right before serialization of method starts.
Pass the method name


### `getMethodBeforeCallbacks(): array`

Called right before serialization of method starts.
Pass the method name


### `getConstructorCallbacks(): array`

Called right after deserialization of object, passing the final object.



### `getConstructorBeforeCallbacks(): array`

Called right before deserialization of object.
Pass only the constructor name


### `getConstructorSerializeCallbacks(): array`

Called right before serialization of constructor.
Passed the object, will return a modified version.


### `getTypeMismatchCallbacks(): array`

Called if objects of the specified type cannot be serialized.
Passed the unserializable object,
will try to convert it to an object of the proper type.


### `init(): void`

Blockingly init.



### `initAsynchronously(): \Generator`

Asynchronously init.


#### See also: 
* `\Generator`




### `inited(): bool`

Check if we've already inited.



### `forceInit(bool $inited): void`

Mark instance as (de)inited forcefully.


Parameters:
* `$inited`: `bool` Whether to mark the instance as inited or deinited  



### `methodCall(string $method, array|\Generator $args, array $aargs): mixed`

Synchronous wrapper for methodCall.


Parameters:
* `$method`: `string` Method name  
* `$args`: `array|\Generator` Arguments  
  Full type:
  ```
  array|\Generator<mixed, mixed, mixed, array>
  ```
* `$aargs`: `array` Additional arguments  


#### See also: 
* `\Generator`




### `methodCallAsyncRead(string $method, array|\Generator $args, array $aargs): \Generator`

Call method and wait asynchronously for response.
If the $aargs['noResponse'] is true, will not wait for a response.

Parameters:
* `$method`: `string` Method name  
* `$args`: `array|\Generator` Arguments  
  Full type:
  ```
  array|\Generator<mixed, mixed, mixed, array>
  ```
* `$aargs`: `array` Additional arguments  


#### See also: 
* `\Generator`




### `methodCallAsyncWrite(string $method, array|\Generator $args, array $aargs): \Generator`

Call method and make sure it is asynchronously sent.


Parameters:
* `$method`: `string` Method name  
* `$args`: `array|\Generator` Arguments  
  Full type:
  ```
  array|\Generator<mixed, mixed, mixed, array>
  ```
* `$aargs`: `array` Additional arguments  


#### See also: 
* `\Generator`




### `toSupergroup(int $id): float|int`

Convert MTProto channel ID to bot API channel ID.


Parameters:
* `$id`: `int` MTProto channel ID  



### `fromSupergroup(int $id): float|int`

Convert bot API channel ID to MTProto channel ID.


Parameters:
* `$id`: `int` Bot API channel ID  



### `isSupergroup(int $id): bool`

Check whether provided bot API ID is a channel.


Parameters:
* `$id`: `int` Bot API ID  



### `addUser(array $user): \Generator`

Add user info.


Parameters:
* `$user`: `array` User info  


#### See also: 
* `\Generator`




### `peerIsset(mixed $id): \Generator`

Check if peer is present in internal peer database.


Parameters:
* `$id`: `mixed` Peer  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|array, mixed, bool>
```
#### See also: 
* `\Amp\Promise`
* `\Generator`




### `getFolderId(mixed $id): ?int`

Get folder ID from object.


Parameters:
* `$id`: `mixed` Object  



### `getId(mixed $id): int`

Get bot API ID from peer object.


Parameters:
* `$id`: `mixed` Peer  



### `getInfo(mixed $id, bool $recursive): \Generator Info object`

Get info about peer, returns an Info object.


Parameters:
* `$id`: `mixed` Peer  
* `$recursive`: `bool` Internal  


Return value: Info object

Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<string>|array, mixed, array{InputPeer: array{_: string, user_id?: mixed, access_hash?: mixed, min?: mixed, chat_id?: mixed, channel_id?: mixed}, Peer: array{_: string, user_id?: mixed, chat_id?: mixed, channel_id?: mixed}, DialogPeer: array{_: string, peer: array{_: string, user_id?: mixed, chat_id?: mixed, channel_id?: mixed}}, NotifyPeer: array{_: string, peer: array{_: string, user_id?: mixed, chat_id?: mixed, channel_id?: mixed}}, InputDialogPeer: array{_: string, peer: array{_: string, user_id?: mixed, access_hash?: mixed, min?: mixed, chat_id?: mixed, channel_id?: mixed}}, InputNotifyPeer: array{_: string, peer: array{_: string, user_id?: mixed, access_hash?: mixed, min?: mixed, chat_id?: mixed, channel_id?: mixed}}, bot_api_id: int|string, user_id?: int, chat_id?: int, channel_id?: int, InputUser?: array{_: string, user_id?: int, access_hash?: mixed, min?: bool}, InputChannel?: array{_: string, channel_id: int, access_hash: mixed, min: bool}, type: string}>
```
#### See also: 
* [https://docs.madelineproto.xyz/Info.html](https://docs.madelineproto.xyz/Info.html)
* `\Amp\Promise`
* `\Generator`




### `fullChatLastUpdated(mixed $id): \Generator<int>`

When were full info for this chat last cached.


Parameters:
* `$id`: `mixed` Chat ID  


#### See also: 
* `\Generator`




### `getFullInfo(mixed $id): \Generator FullInfo object`

Get full info about peer, returns an FullInfo object.


Parameters:
* `$id`: `mixed` Peer  


Return value: FullInfo object

Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|array, mixed, array>
```
#### See also: 
* [https://docs.madelineproto.xyz/FullInfo.html](https://docs.madelineproto.xyz/FullInfo.html)
* `\Amp\Promise`
* `\Generator`




### `getPwrChat(mixed $id): \Generator<array> Chat object`

Get full info about peer (including full list of channel members), returns a Chat object.


Parameters:
* `$id`: `mixed` Peer  


Return value: Chat object

#### See also: 
* [https://docs.madelineproto.xyz/Chat.html](https://docs.madelineproto.xyz/Chat.html)




### `resolveUsername(string $username): \Generator`

Resolve username (use getInfo instead).


Parameters:
* `$username`: `string` Username  


#### See also: 
* `\Generator`




### `uploadFromUrl(string|\danog\MadelineProto\FileCallbackInterface $url, int $size, string $fileName, callable $cb, bool $encrypted): \Generator`

Upload file from URL.


Parameters:
* `$url`: `string|\danog\MadelineProto\FileCallbackInterface` URL of file  
* `$size`: `int` Size of file  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\Http\Client\Response>|\Amp\Promise<int>|\Amp\Promise<null|string>|\danog\MadelineProto\Stream\StreamInterface|array|int|mixed, mixed, mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`
* `\Amp\Http\Client\Response`
* `\danog\MadelineProto\Stream\StreamInterface`
* `\Generator`




### `uploadFromCallable(mixed $callable, int $size, string $mime, string $fileName, callable $cb, bool $seekable, bool $encrypted): \Generator`

Upload file from callable.
The callable must accept two parameters: int $offset, int $size
The callable must return a string with the contest of the file at the specified offset and size.

Parameters:
* `$callable`: `mixed` Callable  
* `$size`: `int` File size  
* `$mime`: `string` Mime type  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$seekable`: `bool` Whether chunks can be fetched out of order  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Generator<int, \Amp\Promise|\Amp\Promise<array>, mixed, array{_: string, id: string, parts: int, name: string, mime_type: string, key_fingerprint?: mixed, key?: mixed, iv?: mixed, md5_checksum: string}>
```
#### See also: 
* `\Amp\Promise`
* `\Generator`




### `uploadFromTgfile(mixed $media, callable $cb, bool $encrypted): \Generator`

Reupload telegram file.


Parameters:
* `$media`: `mixed` Telegram file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|array, mixed, mixed>
```
#### See also: 
* `\Amp\Promise`
* `\Generator`




### `getFileInfo(mixed $constructor): \Generator<array>`

Get info about file.


Parameters:
* `$constructor`: `mixed` File ID  


#### See also: 
* `\Generator`




### `getPropicInfo(mixed $messageMedia): \Generator<array>`

Get download info of the propic of a user
Returns an array with the following structure:.
`$info['ext']` - The file extension
`$info['name']` - The file name, without the extension
`$info['mime']` - The file mime type
`$info['size']` - The file size

Parameters:
* `$messageMedia`: `mixed` File ID  


#### See also: 
* `\Generator`




### `extractBotAPIFile(array $info): ?array`

Extract file info from bot API message.


Parameters:
* `$info`: `array` Bot API message object  



### `getDownloadInfo(mixed $messageMedia): \Generator<array>`

Get download info of file
Returns an array with the following structure:.
`$info['ext']` - The file extension
`$info['name']` - The file name, without the extension
`$info['mime']` - The file mime type
`$info['size']` - The file size

Parameters:
* `$messageMedia`: `mixed` File ID  


#### See also: 
* `\Generator`




### `downloadToDir(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $dir, callable $cb): \Generator`

Download file to directory.


Parameters:
* `$messageMedia`: `mixed` File to download  
* `$dir`: `string|\danog\MadelineProto\FileCallbackInterface` Directory where to download the file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\File\File>|\Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<callable|null>|\Amp\Promise<mixed>|array|bool|mixed, mixed, false|string>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`
* `\Amp\File\File`
* `\Amp\Ipc\Sync\ChannelledSocket`
* `\Generator`




### `downloadToFile(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $file, callable $cb): \Generator Downloaded file path`

Download file.


Parameters:
* `$messageMedia`: `mixed` File to download  
* `$file`: `string|\danog\MadelineProto\FileCallbackInterface` Downloaded file path  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


Return value: Downloaded file path

Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\File\File>|\Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<callable|null>|\Amp\Promise<mixed>|array|bool|mixed, mixed, false|string>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`
* `\Amp\File\File`
* `\Amp\Ipc\Sync\ChannelledSocket`
* `\Generator`




### `downloadToCallable(mixed $messageMedia, callable|\danog\MadelineProto\FileCallbackInterface $callable, callable $cb, bool $seekable, int $offset, int $end, int $part_size): \Generator`

Download file to callable.
The callable must accept two parameters: string $payload, int $offset
The callable will be called (possibly out of order, depending on the value of $seekable).
The callable should return the number of written bytes.

Parameters:
* `$messageMedia`: `mixed` File to download  
* `$callable`: `callable|\danog\MadelineProto\FileCallbackInterface` Chunk callback  
* `$cb`: `callable` Status callback (DEPRECATED, use FileCallbackInterface)  
* `$seekable`: `bool` Whether the callable can be called out of order  
* `$offset`: `int` Offset where to start downloading  
* `$end`: `int` Offset where to stop downloading (inclusive)  
* `$part_size`: `int` Size of each chunk  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|array, mixed, true>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`
* `\Generator`




### `downloadToBrowser(array|string $messageMedia, callable $cb): \Generator`

Download file to browser.
Supports HEAD requests and content-ranges for parallel and resumed downloads.

Parameters:
* `$messageMedia`: `array|string` File to download  
* `$cb`: `callable` Status callback (can also use FileCallback)  


#### See also: 
* `\Generator`




### `downloadToStream(mixed $messageMedia, mixed|\danog\MadelineProto\FileCallbackInterface $stream, callable $cb, int $offset, int $end): \Generator`

Download file to stream.


Parameters:
* `$messageMedia`: `mixed` File to download  
* `$stream`: `mixed|\danog\MadelineProto\FileCallbackInterface` Stream where to download file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$offset`: `int` Offset where to start downloading  
* `$end`: `int` Offset where to end download  


Fully typed return value:
```
\Generator<int, \Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<mixed>|mixed, mixed, mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Ipc\Sync\ChannelledSocket`
* `\Amp\Promise`
* `\Generator`




### `downloadToResponse(array|string $messageMedia, \ServerRequest $request, callable $cb): \Generator Returned response`

Download file to amphp/http-server response.
Supports HEAD requests and content-ranges for parallel and resumed downloads.

Parameters:
* `$messageMedia`: `array|string` File to download  
* `$request`: `\ServerRequest` Request  
* `$cb`: `callable` Status callback (can also use FileCallback)  


Return value: Returned response

Fully typed return value:
```
\Generator<mixed, array, mixed, \Amp\Http\Server\Response>
```
#### See also: 
* `\ServerRequest`
* `\Amp\Http\Server\Response`
* `\Generator`




### `uploadEncrypted(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb): \Generator`

Upload file to secret chat.


Parameters:
* `$file`: `\danog\MadelineProto\FileCallbackInterface|string|array` File, URL or Telegram file to upload  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\File\File>|\Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<int>|\Amp\Promise<mixed>|\Amp\Promise<null|string>|\danog\MadelineProto\Stream\StreamInterface|array|int|mixed, mixed, mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`
* `\Amp\File\File`
* `\Amp\Ipc\Sync\ChannelledSocket`
* `\danog\MadelineProto\Stream\StreamInterface`
* `\Generator`




### `upload(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb, bool $encrypted): \Generator`

Upload file.


Parameters:
* `$file`: `\danog\MadelineProto\FileCallbackInterface|string|array` File, URL or Telegram file to upload  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\File\File>|\Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<int>|\Amp\Promise<mixed>|\Amp\Promise<null|string>|\danog\MadelineProto\Stream\StreamInterface|array|int|mixed, mixed, mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`
* `\Amp\File\File`
* `\Amp\Ipc\Sync\ChannelledSocket`
* `\danog\MadelineProto\Stream\StreamInterface`
* `\Generator`




### `uploadFromStream(mixed $stream, int $size, string $mime, string $fileName, callable $cb, bool $encrypted): \Generator`

Upload file from stream.


Parameters:
* `$stream`: `mixed` PHP resource or AMPHP async stream  
* `$size`: `int` File size  
* `$mime`: `string` Mime type  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<int>|\Amp\Promise<null|string>|\danog\MadelineProto\Stream\StreamInterface|array|int|mixed, mixed, mixed>
```
#### See also: 
* `\Amp\Promise`
* `\danog\MadelineProto\Stream\StreamInterface`
* `\Generator`




### `acceptSecretChat(array $params): \Generator`

Accept secret chat.


Parameters:
* `$params`: `array` Secret chat ID  


#### See also: 
* `\Generator`




### `requestSecretChat(mixed $user): \Generator`

Request secret chat.


Parameters:
* `$user`: `mixed` User to start secret chat with  


#### See also: 
* `\Generator`




### `rekey(int $chat): \Generator`

Rekey secret chat.


Parameters:
* `$chat`: `int` Secret chat to rekey  


#### See also: 
* `\Generator`




### `secretChatStatus(int $chat): \int One of MTProto::SECRET_EMPTY, MTProto::SECRET_REQUESTED, MTProto::SECRET_READY`

Get secret chat status.


Parameters:
* `$chat`: `int` Chat ID  


Return value: One of MTProto::SECRET_EMPTY, MTProto::SECRET_REQUESTED, MTProto::SECRET_READY


### `getSecretChat(array|int $chat): array`

Get secret chat.


Parameters:
* `$chat`: `array|int` Secret chat ID  



### `hasSecretChat(array|int $chat): bool`

Check whether secret chat exists.


Parameters:
* `$chat`: `array|int` Secret chat ID  



### `discardSecretChat(int $chat): \Generator`

Discard secret chat.


Parameters:
* `$chat`: `int` Secret chat ID  


#### See also: 
* `\Generator`




### `mbStrlen(string $text): float|int`

Get Telegram UTF-8 length of string.


Parameters:
* `$text`: `string` Text  



### `mbSubstr(string $text, int $offset, ?int $length): string`

Telegram UTF-8 multibyte substring.


Parameters:
* `$text`: `string` Text to substring  
* `$offset`: `int` Offset  
* `$length`: `?int` Length  



### `mbStrSplit(string $text, int $length): array`

Telegram UTF-8 multibyte split.


Parameters:
* `$text`: `string` Text  
* `$length`: `int` Length  



### `MTProtoToBotAPI(array $data): \Generator<array>`

Convert MTProto parameters to bot API parameters.


Parameters:
* `$data`: `array` Data  


#### See also: 
* `\Generator`




### `botAPIToMTProto(array $arguments): \Generator<array>`

Convert bot API parameters to MTProto parameters.


Parameters:
* `$arguments`: `array` Arguments  


#### See also: 
* `\Generator`




### `unpackFileId(string $fileId): \array Unpacked file ID`

Unpack bot API file ID.


Parameters:
* `$fileId`: `string` Bot API file ID  


Return value: Unpacked file ID


### `tdcliToTd(array $params, array $key): array`

Convert tdcli parameters to tdcli.


Parameters:
* `$params`: `array` Params  
* `$key`: `array` Key  



### `tdToMTProto(array $params): \Generator<array>`

Convert TD to MTProto parameters.


Parameters:
* `$params`: `array` Parameters  


#### See also: 
* `\Generator`




### `MTProtoToTdcli(mixed $params): \Generator`

MTProto to TDCLI params.


Parameters:
* `$params`: `mixed` Params  


#### See also: 
* `\Generator`




### `MTProtoToTd(mixed $params): \Generator`

MTProto to TD params.


Parameters:
* `$params`: `mixed` Params  


#### See also: 
* `\Generator`




### `tdToTdcli(mixed $params): mixed`

Convert TD parameters to tdcli.


Parameters:
* `$params`: `mixed` Parameters  



### `requestCall(mixed $user): \Generator`

Request VoIP call.


Parameters:
* `$user`: `mixed` User  


#### See also: 
* `\Generator`




### `acceptCall(array $call): \Generator`

Accept call.


Parameters:
* `$call`: `array` Call  


#### See also: 
* `\Generator`




### `confirmCall(array $params): \Generator`

Confirm call.


Parameters:
* `$params`: `array` Params  


#### See also: 
* `\Generator`




### `completeCall(array $params): \Generator`

Complete call handshake.


Parameters:
* `$params`: `array` Params  


#### See also: 
* `\Generator`




### `callStatus(int $id): int`

Get call status.


Parameters:
* `$id`: `int` Call ID  



### `getCall(int $call): array`

Get call info.


Parameters:
* `$call`: `int` Call ID  



### `discardCall(array $call, array $reason, array $rating, bool $need_debug): \Generator`

Discard call.


Parameters:
* `$call`: `array` Call  
* `$reason`: `array`   
* `$rating`: `array` Rating  
* `$need_debug`: `bool` Need debug?  


#### See also: 
* `\Generator`




### `getDialogs(bool $force): \Generator`

Get dialog peers.


Parameters:
* `$force`: `bool` Whether to refetch all dialogs ignoring cache  


Fully typed return value:
```
\Generator<int, \Amp\Promise<bool>, mixed, list<mixed>>
```
#### See also: 
* `\Amp\Promise`
* `\Generator`




### `getFullDialogs(bool $force): \Generator`

Get full info of all dialogs.


Parameters:
* `$force`: `bool` Whether to refetch all dialogs ignoring cache  


#### See also: 
* `\Generator`




### `setEventHandler(class-string<\danog\MadelineProto\EventHandler> $eventHandler): \Generator`

Set event handler.


Parameters:
* `$eventHandler`: `class-string<\danog\MadelineProto\EventHandler>` Event handler  


#### See also: 
* [`\danog\MadelineProto\EventHandler`: Event handler.](./EventHandler.md)
* `\Generator`




### `unsetEventHandler(bool $disableUpdateHandling): void`

Unset event handler.


Parameters:
* `$disableUpdateHandling`: `bool` Whether to also disable internal update handling (will cause errors, otherwise will simply use the NOOP handler)  



### `getEventHandler(): \danog\MadelineProto\EventHandler`

Get event handler.


#### See also: 
* [`\danog\MadelineProto\EventHandler`: Event handler.](./EventHandler.md)




### `hasEventHandler(): bool`

Check if an event handler instance is present.



### `setWebhook(string $hook_url, string $pem_path): void`

Set webhook update handler.


Parameters:
* `$hook_url`: `string` Webhook URL  
* `$pem_path`: `string` PEM path for self-signed certificate  



### `setCallback(callable $callback): void`

Set update handling callback.


Parameters:
* `$callback`: `callable` Callback  



### `logout(): \Generator`

Log out currently logged in user.


#### See also: 
* `\Generator`




### `botLogin(string $token): \Generator`

Login as bot.


Parameters:
* `$token`: `string` Bot token  


#### See also: 
* `\Generator`




### `phoneLogin(string $number, int $sms_type): \Generator`

Login as user.


Parameters:
* `$number`: `string` Phone number  
* `$sms_type`: `int` SMS type  


#### See also: 
* `\Generator`




### `completePhoneLogin(string $code): \Generator`

Complet user login using login code.


Parameters:
* `$code`: `string` Login code  


#### See also: 
* `\Generator`




### `importAuthorization(mixed $authorization): \Generator`

Import authorization.


Parameters:
* `$authorization`: `mixed` Authorization info  


#### See also: 
* `\Generator`




### `exportAuthorization(): \Generator`

Export authorization.


Fully typed return value:
```
\Generator<mixed, array|bool, mixed, array{0: int|string, 1: string}>
```
#### See also: 
* `\Generator`




### `completeSignup(string $first_name, string $last_name): \Generator`

Complete signup to Telegram.


Parameters:
* `$first_name`: `string` First name  
* `$last_name`: `string` Last name  


#### See also: 
* `\Generator`




### `complete2faLogin(string $password): \Generator`

Complete 2FA login.


Parameters:
* `$password`: `string` Password  


#### See also: 
* `\Generator`




### `update2fa(array $params): \Generator`

Update the 2FA password.
The params array can contain password, new_password, email and hint params.

Parameters:
* `$params`: `array` The params  


#### See also: 
* `\Generator`




### `initSelfRestart(): void`

Initialize self-restart hack.



### `loop(callable|null $callback): \Generator`

Start MadelineProto's update handling loop, or run the provided async callable.


Parameters:
* `$callback`: `callable|null` Async callable to run  


#### See also: 
* `\Generator`




### `stop(): void`

Stop update loop.



### `restart(): void`

Restart update loop.



### `loopFork(): \Amp\Promise`

Start MadelineProto's update handling loop in background.


#### See also: 
* `\Amp\Promise`




### `closeConnection(string $message): void`

Close connection with client, connected via web.


Parameters:
* `$message`: `string` Message  



### `setNoop(): void`

Set NOOP update handler, ignoring all updates.



### `start(): \Generator`

Log in to telegram (via CLI or web).


#### See also: 
* `\Generator`




### `getWebTemplate(): string`

Get web template.



### `setWebTemplate(string $template): void`

Set web template.


Parameters:
* `$template`: `string` Template  



### `checkTos(): \Generator`

Check for terms of service update.


#### See also: 
* `\Generator`




### `acceptTos(): \Generator`

Accept terms of service update.


#### See also: 
* `\Generator`




### `declineTos(): \Generator`

Decline terms of service update.
THIS WILL DELETE YOUR ACCOUNT!

#### See also: 
* `\Generator`




---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
