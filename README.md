# Deferred promise

An elegant and simple way to use a promise


Installation & Usage
--------------------

```bash
yarn add diferred-promise
```

```javascript
import DiferredPromise from "diferred-promise"

export default function () {
  let deferred = new DiferredPromise()

  doSomething()
    .then(someParams => deferred.resolve(someParams))
    .catch(() => deferred.reject())
    
  return deferred.promise
}
```