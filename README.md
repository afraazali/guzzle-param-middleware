Guzzle Middleware that adds one or more query parameters to all requests
for a client.

[![Build Status](https://travis-ci.org/emarref/guzzle-param-middleware.svg?branch=master)](https://travis-ci.org/emarref/guzzle-param-middleware)

## Usage

```php
$paramMiddleware = new Emarref\Guzzle\Middleware\ParamMiddleware(['foo' => 'bar']);
$stack = GuzzleHttp\HandlerStack::create();
$stack->push($paramMiddleware);
$client = new GuzzleHttp\Client(['handler' => $stack]);
```

All requests made by the guzzle client above will include `foo=bar` in
the GET query.
