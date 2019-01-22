# ULID Library (JavaScript)

This is a browser JavaScript library for generating [Universally Unique
Lexicographically Sortable Identifiers][ulid] (ULIDs). With modern
browsers on modern hardware, it can generate 1.5 million ULIDs per
second.

The API is a single constructor. It constructs a closure that generates
monotonic ULIDs each time it's invoked.

```js
let generator = ULID();
let ulid0 = generator();
let ulid1 = generator();
assert(ulid0 < ulid1);
```

The generator itself makes no allocations when generating ULIDs, except
for the returned ULID string.


[ulid]: https://github.com/ulid/spec
