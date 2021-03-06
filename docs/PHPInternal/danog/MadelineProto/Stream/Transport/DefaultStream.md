---
title: danog\MadelineProto\Stream\Transport\DefaultStream: Default stream wrapper.
description: Manages reading data in chunks

---
# `danog\MadelineProto\Stream\Transport\DefaultStream`
[Back to index](../../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Default stream wrapper.  

Manages reading data in chunks


## Method list:
* `getStream(): \Amp\Socket\EncryptableSocket`
* `read(): \Amp\Promise`
* `write(string $data): \Amp\Promise`
* `disconnect(): void`
* `close(): void`
* `getSocket(): \Amp\Socket\EncryptableSocket`

## Methods:
### `getStream(): \Amp\Socket\EncryptableSocket`




#### See also: 
* `\Amp\Socket\EncryptableSocket`




### `read(): \Amp\Promise`

Async chunked read.


#### See also: 
* `\Amp\Promise`




### `write(string $data): \Amp\Promise`

Async write.


Parameters:
* `$data`: `string` Data to write  


#### See also: 
* `\Amp\Promise`




### `disconnect(): void`

Close.



### `close(): void`

Close.



### `getSocket(): \Amp\Socket\EncryptableSocket`

{@inheritdoc}


#### See also: 
* `\Amp\Socket\EncryptableSocket`




---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
