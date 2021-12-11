This PHP library implements a subscriber for PubSubHubbub.

It was written by [Josh Fraser](http://joshfraser.com) and is released under the Apache 2.0 License

Modified by Andrei Telteu to work with the latest modifications by Youtube's pubsubhubbub service to allow challenge verification.

# Install
Install this fork using this command:
```bash
composer require onlinedigital/pubsubhubbub-php-subscriber
```

# Usage
```php
use \Pubsubhubbub\Subscriber\Subscriber;

$hub_url      = "http://pubsubhubbub.appspot.com";
$callback_url = "put your own endpoint here";

// create a new subscriber
$s = new Subscriber($hub_url, $callback_url);

$feed = "http://feeds.feedburner.com/onlineaspect";

// subscribe to a feed
$s->subscribe($feed);

// unsubscribe from a feed
$s->unsubscribe($feed);
```
