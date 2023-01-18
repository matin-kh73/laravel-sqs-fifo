[![License](http://poser.pugx.org/culturalinfusion/laravel-sqs-fifo/license)](https://packagist.org/packages/culturalinfusion/laravel-sqs-fifo)

# Laravel SQS FIFO

## Table of contents

* [Intro](#intro)
* [How to use](#how-to-use)
* [Testing](#testing)

## Intro

Laravel SQS FIFO provides a queue driver for Laravel.

## How to use

1. Run `composer require culturalinfusion/laravel-sqs-fifo` 
2. Update `config/queue.php` of the application with sample from `config/queue.php` of package (Currently Laravel does not support automated config merge for multi-dimensional configuration array, so needs to be done manually):
  + SQS endpoint structure is `https://sqs.${AWS_REGION}.amazonaws.com/${prefix}/${queue_name_prefix}${queue}${suffix}.fifo` 
  + No need to add `.fifo` to queue name in application side, package takes care of it.

## Testing

To run tests using PHPUnit, execute `./vendor/bin/phpunit` .
