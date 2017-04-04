# api documentation for  [limiter (v1.1.0)](https://github.com/jhurliman/node-rate-limiter#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-limiter.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-limiter) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-limiter.svg)](https://travis-ci.org/npmdoc/node-npmdoc-limiter)
#### A generic rate limiter for node.js. Useful for API clients, web crawling, or other tasks that need to be throttled

[![NPM](https://nodei.co/npm/limiter.png?downloads=true)](https://www.npmjs.com/package/limiter)

[![apidoc](https://npmdoc.github.io/node-npmdoc-limiter/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-limiter_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-limiter/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-limiter/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-limiter/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "John Hurliman",
        "email": "jhurliman@jhurliman.org"
    },
    "bugs": {
        "url": "http://github.com/jhurliman/node-rate-limiter/issues"
    },
    "dependencies": {},
    "description": "A generic rate limiter for node.js. Useful for API clients, web crawling, or other tasks that need to be throttled",
    "devDependencies": {
        "assert": "1.3.0",
        "vows": "0.8.1"
    },
    "directories": {
        "lib": "./lib/"
    },
    "dist": {
        "shasum": "6e2bd12ca3fcdaa11f224e2e53c896df3f08d913",
        "tarball": "https://registry.npmjs.org/limiter/-/limiter-1.1.0.tgz"
    },
    "gitHead": "bf4286a31db48dec2a1a0029bf2ab703dd016b12",
    "homepage": "https://github.com/jhurliman/node-rate-limiter#readme",
    "keywords": [
        "rate",
        "limiting",
        "throttling"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "http://github.com/jhurliman/node-rate-limiter/raw/master/LICENSE.txt"
        }
    ],
    "main": "./index.js",
    "maintainers": [
        {
            "name": "jhurliman",
            "email": "jhurliman@cull.tv"
        }
    ],
    "name": "limiter",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/jhurliman/node-rate-limiter.git"
    },
    "scripts": {
        "test": "vows --spec"
    },
    "version": "1.1.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module limiter](#apidoc.module.limiter)
1.  [function <span class="apidocSignatureSpan">limiter.</span>RateLimiter (tokensPerInterval, interval, fireImmediately)](#apidoc.element.limiter.RateLimiter)
1.  [function <span class="apidocSignatureSpan">limiter.</span>TokenBucket (bucketSize, tokensPerInterval, interval, parentBucket)](#apidoc.element.limiter.TokenBucket)
1.  object <span class="apidocSignatureSpan">limiter.</span>RateLimiter.prototype
1.  object <span class="apidocSignatureSpan">limiter.</span>TokenBucket.prototype

#### [module limiter.RateLimiter](#apidoc.module.limiter.RateLimiter)
1.  [function <span class="apidocSignatureSpan">limiter.</span>RateLimiter (tokensPerInterval, interval, fireImmediately)](#apidoc.element.limiter.RateLimiter.RateLimiter)

#### [module limiter.RateLimiter.prototype](#apidoc.module.limiter.RateLimiter.prototype)
1.  boolean <span class="apidocSignatureSpan">limiter.RateLimiter.prototype.</span>fireImmediately
1.  [function <span class="apidocSignatureSpan">limiter.RateLimiter.prototype.</span>getTokensRemaining ()](#apidoc.element.limiter.RateLimiter.prototype.getTokensRemaining)
1.  [function <span class="apidocSignatureSpan">limiter.RateLimiter.prototype.</span>removeTokens (count, callback)](#apidoc.element.limiter.RateLimiter.prototype.removeTokens)
1.  [function <span class="apidocSignatureSpan">limiter.RateLimiter.prototype.</span>tryRemoveTokens (count)](#apidoc.element.limiter.RateLimiter.prototype.tryRemoveTokens)
1.  number <span class="apidocSignatureSpan">limiter.RateLimiter.prototype.</span>curIntervalStart
1.  number <span class="apidocSignatureSpan">limiter.RateLimiter.prototype.</span>tokensThisInterval
1.  object <span class="apidocSignatureSpan">limiter.RateLimiter.prototype.</span>tokenBucket

#### [module limiter.TokenBucket](#apidoc.module.limiter.TokenBucket)
1.  [function <span class="apidocSignatureSpan">limiter.</span>TokenBucket (bucketSize, tokensPerInterval, interval, parentBucket)](#apidoc.element.limiter.TokenBucket.TokenBucket)

#### [module limiter.TokenBucket.prototype](#apidoc.module.limiter.TokenBucket.prototype)
1.  [function <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>drip ()](#apidoc.element.limiter.TokenBucket.prototype.drip)
1.  [function <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>removeTokens (count, callback)](#apidoc.element.limiter.TokenBucket.prototype.removeTokens)
1.  [function <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>tryRemoveTokens (count)](#apidoc.element.limiter.TokenBucket.prototype.tryRemoveTokens)
1.  number <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>bucketSize
1.  number <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>content
1.  number <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>interval
1.  number <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>lastDrip
1.  number <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>tokensPerInterval
1.  object <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>parentBucket



# <a name="apidoc.module.limiter"></a>[module limiter](#apidoc.module.limiter)

#### <a name="apidoc.element.limiter.RateLimiter"></a>[function <span class="apidocSignatureSpan">limiter.</span>RateLimiter (tokensPerInterval, interval, fireImmediately)](#apidoc.element.limiter.RateLimiter)
- description and source-code
```javascript
RateLimiter = function (tokensPerInterval, interval, fireImmediately) {
  this.tokenBucket = new TokenBucket(tokensPerInterval, tokensPerInterval,
    interval, null);

  // Fill the token bucket to start
  this.tokenBucket.content = tokensPerInterval;

  this.curIntervalStart = +new Date();
  this.tokensThisInterval = 0;
  this.fireImmediately = fireImmediately;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.limiter.TokenBucket"></a>[function <span class="apidocSignatureSpan">limiter.</span>TokenBucket (bucketSize, tokensPerInterval, interval, parentBucket)](#apidoc.element.limiter.TokenBucket)
- description and source-code
```javascript
TokenBucket = function (bucketSize, tokensPerInterval, interval, parentBucket) {
  this.bucketSize = bucketSize;
  this.tokensPerInterval = tokensPerInterval;

  if (typeof interval === 'string') {
    switch (interval) {
      case 'sec': case 'second':
        this.interval = 1000; break;
      case 'min': case 'minute':
        this.interval = 1000 * 60; break;
      case 'hr': case 'hour':
        this.interval = 1000 * 60 * 60; break;
      case 'day':
        this.interval = 1000 * 60 * 60 * 24; break;
    }
  } else {
    this.interval = interval;
  }

  this.parentBucket = parentBucket;
  this.content = 0;
  this.lastDrip = +new Date();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.limiter.RateLimiter"></a>[module limiter.RateLimiter](#apidoc.module.limiter.RateLimiter)

#### <a name="apidoc.element.limiter.RateLimiter.RateLimiter"></a>[function <span class="apidocSignatureSpan">limiter.</span>RateLimiter (tokensPerInterval, interval, fireImmediately)](#apidoc.element.limiter.RateLimiter.RateLimiter)
- description and source-code
```javascript
RateLimiter = function (tokensPerInterval, interval, fireImmediately) {
  this.tokenBucket = new TokenBucket(tokensPerInterval, tokensPerInterval,
    interval, null);

  // Fill the token bucket to start
  this.tokenBucket.content = tokensPerInterval;

  this.curIntervalStart = +new Date();
  this.tokensThisInterval = 0;
  this.fireImmediately = fireImmediately;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.limiter.RateLimiter.prototype"></a>[module limiter.RateLimiter.prototype](#apidoc.module.limiter.RateLimiter.prototype)

#### <a name="apidoc.element.limiter.RateLimiter.prototype.getTokensRemaining"></a>[function <span class="apidocSignatureSpan">limiter.RateLimiter.prototype.</span>getTokensRemaining ()](#apidoc.element.limiter.RateLimiter.prototype.getTokensRemaining)
- description and source-code
```javascript
getTokensRemaining = function () {
  this.tokenBucket.drip();
  return this.tokenBucket.content;
}
```
- example usage
```shell
...
To get the number of remaining tokens **outside** the 'removeTokens'-callback
simply use the 'getTokensRemaining'-method.
'''javascript
var RateLimiter = require('limiter').RateLimiter;
var limiter = new RateLimiter(1, 250);

// returns 1 since we did not remove a token and our number of tokens per interval is 1
limiter.getTokensRemaining();
'''

Using the token bucket directly to throttle at the byte level:

'''javascript
var BURST_RATE = 1024 * 1024 * 150; // 150KB/sec burst rate
var FILL_RATE = 1024 * 1024 * 50; // 50KB/sec sustained rate
...
```

#### <a name="apidoc.element.limiter.RateLimiter.prototype.removeTokens"></a>[function <span class="apidocSignatureSpan">limiter.RateLimiter.prototype.</span>removeTokens (count, callback)](#apidoc.element.limiter.RateLimiter.prototype.removeTokens)
- description and source-code
```javascript
removeTokens = function (count, callback) {
  // Make sure the request isn't for more than we can handle
  if (count > this.tokenBucket.bucketSize) {
    process.nextTick(callback.bind(null, 'Requested tokens ' + count +
      ' exceeds maximum tokens per interval ' + this.tokenBucket.bucketSize,
      null));
    return false;
  }

  var self = this;
  var now = Date.now();

  // Advance the current interval and reset the current interval token count
  // if needed
  if (now - this.curIntervalStart >= this.tokenBucket.interval) {
    this.curIntervalStart = now;
    this.tokensThisInterval = 0;
  }

  // If we don't have enough tokens left in this interval, wait until the
  // next interval
  if (count > this.tokenBucket.tokensPerInterval - this.tokensThisInterval) {
    if (this.fireImmediately) {
      process.nextTick(callback.bind(null, null, -1));
    } else {
      var waitInterval = Math.ceil(
        this.curIntervalStart + this.tokenBucket.interval - now);

      setTimeout(function() {
        self.tokenBucket.removeTokens(count, afterTokensRemoved);
      }, waitInterval);
    }
    return false;
  }

  // Remove the requested number of tokens from the token bucket
  return this.tokenBucket.removeTokens(count, afterTokensRemoved);

  function afterTokensRemoved(err, tokensRemaining) {
    if (err) return callback(err, null);

    self.tokensThisInterval += count;
    callback(null, tokensRemaining);
  }
}
```
- example usage
```shell
...
'''javascript
var RateLimiter = require('limiter').RateLimiter;
// Allow 150 requests per hour (the Twitter search limit). Also understands
// 'second', 'minute', 'day', or a number of milliseconds
var limiter = new RateLimiter(150, 'hour');

// Throttle requests
limiter.removeTokens(1, function(err, remainingRequests) {
// err will only be set if we request more than the maximum number of
// requests we set in the constructor

// remainingRequests tells us how many additional requests could be sent
// right this moment

callMyRequestSendingFunction(...);
...
```

#### <a name="apidoc.element.limiter.RateLimiter.prototype.tryRemoveTokens"></a>[function <span class="apidocSignatureSpan">limiter.RateLimiter.prototype.</span>tryRemoveTokens (count)](#apidoc.element.limiter.RateLimiter.prototype.tryRemoveTokens)
- description and source-code
```javascript
tryRemoveTokens = function (count) {
  // Make sure the request isn't for more than we can handle
  if (count > this.tokenBucket.bucketSize)
    return false;

  var now = Date.now();

  // Advance the current interval and reset the current interval token count
  // if needed
  if (now - this.curIntervalStart >= this.tokenBucket.interval) {
    this.curIntervalStart = now;
    this.tokensThisInterval = 0;
  }

  // If we don't have enough tokens left in this interval, return false
  if (count > this.tokenBucket.tokensPerInterval - this.tokensThisInterval)
    return false;

  // Try to remove the requested number of tokens from the token bucket
  return this.tokenBucket.tryRemoveTokens(count);
}
```
- example usage
```shell
...
'''

A synchronous method, tryRemoveTokens(), is available in both RateLimiter and TokenBucket. This will return immediately with a boolean
 value indicating if the token removal was successful.
'''javascript
var RateLimiter = require('limiter').RateLimiter;
var limiter = new RateLimiter(10, 'second');

if (limiter.tryRemoveTokens(5))
  console.log('Tokens removed');
else
  console.log('No tokens removed');
'''

To get the number of remaining tokens **outside** the 'removeTokens'-callback
simply use the 'getTokensRemaining'-method.
...
```



# <a name="apidoc.module.limiter.TokenBucket"></a>[module limiter.TokenBucket](#apidoc.module.limiter.TokenBucket)

#### <a name="apidoc.element.limiter.TokenBucket.TokenBucket"></a>[function <span class="apidocSignatureSpan">limiter.</span>TokenBucket (bucketSize, tokensPerInterval, interval, parentBucket)](#apidoc.element.limiter.TokenBucket.TokenBucket)
- description and source-code
```javascript
TokenBucket = function (bucketSize, tokensPerInterval, interval, parentBucket) {
  this.bucketSize = bucketSize;
  this.tokensPerInterval = tokensPerInterval;

  if (typeof interval === 'string') {
    switch (interval) {
      case 'sec': case 'second':
        this.interval = 1000; break;
      case 'min': case 'minute':
        this.interval = 1000 * 60; break;
      case 'hr': case 'hour':
        this.interval = 1000 * 60 * 60; break;
      case 'day':
        this.interval = 1000 * 60 * 60 * 24; break;
    }
  } else {
    this.interval = interval;
  }

  this.parentBucket = parentBucket;
  this.content = 0;
  this.lastDrip = +new Date();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.limiter.TokenBucket.prototype"></a>[module limiter.TokenBucket.prototype](#apidoc.module.limiter.TokenBucket.prototype)

#### <a name="apidoc.element.limiter.TokenBucket.prototype.drip"></a>[function <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>drip ()](#apidoc.element.limiter.TokenBucket.prototype.drip)
- description and source-code
```javascript
drip = function () {
  if (!this.tokensPerInterval) {
    this.content = this.bucketSize;
    return;
  }

  var now = +new Date();
  var deltaMS = Math.max(now - this.lastDrip, 0);
  this.lastDrip = now;

  var dripAmount = deltaMS * (this.tokensPerInterval / this.interval);
  this.content = Math.min(this.content + dripAmount, this.bucketSize);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.limiter.TokenBucket.prototype.removeTokens"></a>[function <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>removeTokens (count, callback)](#apidoc.element.limiter.TokenBucket.prototype.removeTokens)
- description and source-code
```javascript
removeTokens = function (count, callback) {
  var self = this;

  // Is this an infinite size bucket?
  if (!this.bucketSize) {
    process.nextTick(callback.bind(null, null, count, Number.POSITIVE_INFINITY));
    return true;
  }

  // Make sure the bucket can hold the requested number of tokens
  if (count > this.bucketSize) {
    process.nextTick(callback.bind(null, 'Requested tokens ' + count + ' exceeds bucket size ' +
      this.bucketSize, null));
    return false;
  }

  // Drip new tokens into this bucket
  this.drip();

  // If we don't have enough tokens in this bucket, come back later
  if (count > this.content)
    return comeBackLater();

  if (this.parentBucket) {
    // Remove the requested from the parent bucket first
    return this.parentBucket.removeTokens(count, function(err, remainingTokens) {
      if (err) return callback(err, null);

      // Check that we still have enough tokens in this bucket
      if (count > self.content)
        return comeBackLater();

      // Tokens were removed from the parent bucket, now remove them from
      // this bucket and fire the callback. Note that we look at the current
      // bucket and parent bucket's remaining tokens and return the smaller
      // of the two values
      self.content -= count;
      callback(null, Math.min(remainingTokens, self.content));
    });
  } else {
    // Remove the requested tokens from this bucket and fire the callback
    this.content -= count;
    process.nextTick(callback.bind(null, null, this.content));
    return true;
  }

  function comeBackLater() {
    // How long do we need to wait to make up the difference in tokens?
    var waitInterval = Math.ceil(
      (count - self.content) * (self.interval / self.tokensPerInterval));
    setTimeout(function() { self.removeTokens(count, callback); }, waitInterval);
    return false;
  }
}
```
- example usage
```shell
...
'''javascript
var RateLimiter = require('limiter').RateLimiter;
// Allow 150 requests per hour (the Twitter search limit). Also understands
// 'second', 'minute', 'day', or a number of milliseconds
var limiter = new RateLimiter(150, 'hour');

// Throttle requests
limiter.removeTokens(1, function(err, remainingRequests) {
// err will only be set if we request more than the maximum number of
// requests we set in the constructor

// remainingRequests tells us how many additional requests could be sent
// right this moment

callMyRequestSendingFunction(...);
...
```

#### <a name="apidoc.element.limiter.TokenBucket.prototype.tryRemoveTokens"></a>[function <span class="apidocSignatureSpan">limiter.TokenBucket.prototype.</span>tryRemoveTokens (count)](#apidoc.element.limiter.TokenBucket.prototype.tryRemoveTokens)
- description and source-code
```javascript
tryRemoveTokens = function (count) {
  // Is this an infinite size bucket?
  if (!this.bucketSize)
    return true;

  // Make sure the bucket can hold the requested number of tokens
  if (count > this.bucketSize)
    return false;

  // Drip new tokens into this bucket
  this.drip();

  // If we don't have enough tokens in this bucket, return false
  if (count > this.content)
    return false;

  // Try to remove the requested tokens from the parent bucket
  if (this.parentBucket && !this.parent.tryRemoveTokens(count))
    return false;

  // Remove the requested tokens from this bucket and return
  this.content -= count;
  return true;
}
```
- example usage
```shell
...
'''

A synchronous method, tryRemoveTokens(), is available in both RateLimiter and TokenBucket. This will return immediately with a boolean
 value indicating if the token removal was successful.
'''javascript
var RateLimiter = require('limiter').RateLimiter;
var limiter = new RateLimiter(10, 'second');

if (limiter.tryRemoveTokens(5))
  console.log('Tokens removed');
else
  console.log('No tokens removed');
'''

To get the number of remaining tokens **outside** the 'removeTokens'-callback
simply use the 'getTokensRemaining'-method.
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
