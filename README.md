# Postponed promise

An elegant and simple way to use a promise


Installation & Usage
--------------------

```bash
yarn add postponed-promise
```

```javascript
import PostponedPomise from "postponed-promise"

export default function () {
  let postponedPomise = new PostponedPomise()

  doSomething()
    .then(someParams => postponedPomise.resolve(someParams))
    .catch(postponedPomise.reject)
    
  return postponedPomise.promise
}
```