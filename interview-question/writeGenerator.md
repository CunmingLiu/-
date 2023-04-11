### 手写一个迭代器

```javascript
//手写一个迭代器
function makeIterator(array) {
    var nextIndex = 0;
    return {
        next: function () {
            return nextIndex < array.length
                ? {
                      value: array[nextIndex++],
                      done: false,
                  }
                : {
                      value: undefined,
                      done: true,
                  };
        },
    };
}
const it = makeIterator(["a", "b"]);
console.log(it.next());
console.log(it.next());
console.log(it.next());
```
