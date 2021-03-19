# Event Target Polyfill

A polyfill for `EventTarget` (and `Event`), meant to run in Cloudflare Workers (also works in older version of node or possibly IE 11) that has the most accurate set of characteristics of `EventTarget` that can be provided.


## Usage

```js
import '@worker-tools/event-target-polyfill';

const et = new EventTarget();

et.addEventListener('test', () => console.log('hit!'));

et.dispatchEvent(new Event('test'));
```

## Development

This library has no dependencies. Even development dependencies. To test just run `npm test`. It runs a script, and if it finishes without error, the tests pass.

