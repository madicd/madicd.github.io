---
layout: post
title:  "Make your tests fail"
date:   2023-02-10 21:28:48 +0100
---
Over the years I developed a habit - after I see passing test, I break it hoping to see it to fail.

And sometimes.. **it didn't**.

An obvious cause could be a **bad design** of the tests. Here's few more I remember:

❌ test framework is not used properly

❌ mock has a bug in its logic

❌ `equals` method does not work as expected

Seeing the tests fail when they should is **testing the tests**.

## Example

Starting point is an async function with a passing test.

```javascript
function resolveAfter2Seconds() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('resolved');
    }, 2000);
  });
}

it('passes', () => {
    resolveAfter2Seconds().then(result => {
        expect(result).toBe('resolved');
    });
});
```

When expected value is changed to **something else**, the test still passes.

```javascript
it('passes', () => {
    resolveAfter2Seconds().then(result => {
        expect(result).toBe('something else');
    });
});
```

But.. Why?

It turns out that `then` never gets executed.

This is exactly how I learned about `done` parameter of the test function.

```javascript
it('fails', (done) => {
    resolveAfter2Seconds().then(result => {
        expect(result).toBe('something else');
        done();
    })
    .catch(error => done(error));
});
```