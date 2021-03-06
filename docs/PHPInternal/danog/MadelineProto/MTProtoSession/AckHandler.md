---
title: danog\MadelineProto\MTProtoSession\AckHandler: Manages acknowledgement of messages.
description: 

---
# `danog\MadelineProto\MTProtoSession\AckHandler`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Manages acknowledgement of messages.  




## Method list:
* `ackOutgoingMessageId(string|int $message_id): bool`
* `gotResponseForOutgoingMessage(\danog\MadelineProto\MTProto\OutgoingMessage $message): void`
* `ackIncomingMessage(\danog\MadelineProto\MTProto\IncomingMessage $message): void`
* `hasPendingCalls(): bool`
* `getPendingCalls(): array`

## Methods:
### `ackOutgoingMessageId(string|int $message_id): bool`

Acknowledge outgoing message ID.


Parameters:
* `$message_id`: `string|int` Message Id  



### `gotResponseForOutgoingMessage(\danog\MadelineProto\MTProto\OutgoingMessage $message): void`

We have gotten a response for an outgoing message.


Parameters:
* `$message`: `\danog\MadelineProto\MTProto\OutgoingMessage` Message  


#### See also: 
* `\danog\MadelineProto\MTProto\OutgoingMessage`




### `ackIncomingMessage(\danog\MadelineProto\MTProto\IncomingMessage $message): void`

Acknowledge incoming message ID.


Parameters:
* `$message`: `\danog\MadelineProto\MTProto\IncomingMessage` Message  


#### See also: 
* `\danog\MadelineProto\MTProto\IncomingMessage`




### `hasPendingCalls(): bool`

Check if there are some pending calls.



### `getPendingCalls(): array`

Get all pending calls (also clear pending state requests).



## Properties
* `$shared`: `\DataCenterConnection` 
---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
