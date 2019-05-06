## javascript 常考

### 1. typeof vs instanceof

typeof 对于原始类型，除了null都能正确判断类型。（javascript遗留bug）
```javascript
typeof null // object
```
typeof 对于对象来说，函数为function 其余为object
```javascript
typeof [] // object
typeof {} // object
typeof console.log('123') // function 
```

instanceof 能够正确判断对象的类型，通过原型链来判断
```javascript
const Person = function() {}
const p1 = new Person()
p1 instanceof Person // true
```

instanceof 不能判断原始类型
```javascript
let str = '123123'
str instanceof String // false

let str1 = new String('123123')
str1 instanceof String // true 
```

