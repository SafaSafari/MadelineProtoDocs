---
title: danog\MadelineProto\Settings\Logger: Logger settings.
description: 

---
# `danog\MadelineProto\Settings\Logger`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Logger settings.  




## Method list:
* `getType()`
* `setType(): self`
* `getExtra(): null|callable|string`
* `setExtra(null|callable|string $extra): self`
* `getLevel()`
* `setLevel(): self`
* `getMaxSize(): int`
* `setMaxSize(int $maxSize): self`
* `hasChanged(): bool`

## Methods:
### `getType()`

Get $type Logger type.



### `setType(): self`

Set $type Logger type.



### `getExtra(): null|callable|string`

Get extra parameter for logger.



### `setExtra(null|callable|string $extra): self`

Set extra parameter for logger.


Parameters:
* `$extra`: `null|callable|string` Extra parameter for logger.  



### `getLevel()`

Get logging level.



### `setLevel(): self`

Set logging level.



### `getMaxSize(): int`

Get maximum filesize for logger, in case of file logging.



### `setMaxSize(int $maxSize): self`

Set maximum filesize for logger, in case of file logging.


Parameters:
* `$maxSize`: `int` Maximum filesize for logger, in case of file logging.  



### `hasChanged(): bool`

Get whether this setting was changed, also applies changes.



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
