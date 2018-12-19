## API

### Interface: common

#### splitAt(index, array)

  - `index: `[`<number>`] index defining end of first part and start of second
  - `array: `[`<Array>`] to be split

*Returns:* [`<Array>`] tuple with two parts of the array

Split array into two parts


#### shuffle(arr)

  - `arr: `[`<Array>`]

*Returns:* [`<Array>`]

Shuffle an array


#### range(from, to)

  - `from: `[`<number>`] range start
  - `to: `[`<number>`] range end

*Returns:* [`<Array>`]

Generate int array from given range

*Example:* 
```js
 range(1, 5)
```

*Result:* 
```js
 [1, 2, 3, 4, 5]
```


#### sequence(seq, max)

  - `seq: `[`<Array>`]
  - `max: `[`<number>`] (optional) max

*Returns:* [`<Array>`]

Generate int array from sequence syntax

*Example:* 
```js
 list: sequence([81, 82, 83])
```

*Result:* 
```js
 [81, 82, 83]
```

*Example:* 
```js
 range from..to: sequence([81,,83]) = [81, 82, 83]
```

*Result:* 
```js
 [81, 82, 83]
```

*Example:* 
```js
 range from..count: sequence([81, [3]]) = [81, 82, 83]
```

*Result:* 
```js
 [81, 82, 83]
```

*Example:* 
```js
 range from..max-to: sequence([81, [-2]], 5) = [81, 82, 83]
```

*Result:* 
```js
 [81, 82, 83]
```


#### last(arr)

  - `arr: `[`<Array>`]

*Returns:* `<any>` element

Get last element of array


#### checkLogin(login, required, optional)

  - `login: `[`<string>`] login to test
  - `required: `[`<Array>`] required tests configs
  - `optional: `[`<Array>`] optional tests configs, defalult: `[]`

*Returns:* `<AuthenticationStrength>`

Function that tests the login


#### checkPassword(password, required, optional)

  - `password: `[`<string>`] password to test
  - `required: `[`<Array>`] required tests configs
  - `optional: `[`<Array>`] optional tests configs, default: `[]`

*Returns:* `<AuthenticationStrength>`

Function that tests the password


#### checkLoginPassword(login, password, required, optional)

  - `login: `[`<string>`] login to test
  - `password: `[`<string>`] password to test
  - `required: `[`<Array>`] required tests configs
  - `optional: `[`<Array>`] optional tests configs, default: `[]`

*Returns:* `<AuthenticationStrength>`

Function that tests the login with password


#### BTree()



#### BTree.prototype.constructor()



#### BTree.prototype.get()



#### BTree.prototype.set()



#### BTree.prototype.iterator()



#### BTree.prototype.remove()



#### cache()


*Returns:* `<Cache>`

Create Cache, enhanced Map


#### falseness()


*Returns:* [`<boolean>`] always false

Empty function


#### trueness()


*Returns:* [`<boolean>`] always true

Empty function


#### emptiness()


Empty function


#### nop(callback)

  - `callback: `[`<Function>`] callback to be called with (null)

Empty asynchronous callback-last single-argument function


#### noop(empty, callback)

  - `empty: <any>` incoming value to be ignored
  - `callback: `[`<Function>`] callback to be called with (null, null)

Empty asynchronous callback-last double-argument function


#### once(fn)

  - `fn: `[`<Function>`] (optional)

*Returns:* [`<Function>`] wrapped callback

Wrap function: call once, not null


#### cb()



#### unsafeCallback(args)

  - `args: `[`<Array>`] arguments

*Returns:* [`<Function>`]` | `[`<null>`] callback if any

Extract callback function

It's unsafe: may return null, allows multiple calls


#### extractCallback()



#### cbUnsafe()



#### safeCallback(args)

  - `args: `[`<Array>`] arguments

*Returns:* [`<Function>`] callback or common.emptiness if there is no callback

Extract callback


#### cbExtract()



#### requiredCallback(args)

  - `args: `[`<Array>`] arguments

*Returns:* [`<Function>`] extracted callback

Extract callback

*Throws:* [`<TypeError>`] if there is no callback


#### onceCallback(args)

  - `args: `[`<Array>`] arguments

*Returns:* [`<Function>`] callback or common.emptiness if there is no callback

Extract callback and make it safe

Wrap callback with once()


#### safeFunction(fn)

  - `fn: `[`<Function>`]

*Returns:* [`<Function>`] function or `common.emptiness` if fn is not a function

Check function and make it safe


#### unsafeFunction(fn)

  - `fn: `[`<Function>`]

*Returns:* [`<Function>`]` | `[`<null>`] function or null if fn is not a
    function

Check function


#### id(x)

  - `x: <any>` incoming value which will be returned

*Returns:* `<any>` incoming value

Identity function


#### asyncId(x, callback)

  - `x: <any>` incoming value which will be returned into the callback
  - `callback: `[`<Function>`] callback to be called with first argument
    - `err: `[`<null>`]
    - `data: <any>`

Async identity function


#### isScalar(value)

  - `value: <any>`

*Returns:* [`<boolean>`]

Check if value is scalar


#### copy(ds)

  - `ds: `[`<Object[]>`][`<Object>`] source dataset to be copied

*Returns:* [`<Object[]>`][`<Object>`]

Copy dataset (copy objects to new array)


#### clone(obj)

  - `obj: `[`<Object>`]` | `[`<Array>`]

*Returns:* [`<Object>`]` | `[`<Array>`]

Clone object or array


#### duplicate(obj)

  - `obj: `[`<Object>`]` | `[`<Array>`]

*Returns:* [`<Object>`]` | `[`<Array>`]

Duplicate object or array (properly handles prototype and circular links)


#### getByPath(data, dataPath)

  - `data: `[`<Object>`]
  - `dataPath: `[`<string>`] dot-separated path

*Returns:* `<any>` value

Read property by dot-separated path


#### setByPath(data, dataPath, value)

  - `data: `[`<Object>`]
  - `dataPath: `[`<string>`] dot-separated path
  - `value: <any>` new value

Set property by dot-separated path


#### deleteByPath(data, dataPath)

  - `data: `[`<Object>`]
  - `dataPath: `[`<string>`] dot-separated path

*Returns:* [`<boolean>`]

Delete property by dot-separated path


#### merge(args)

  - `args: `[`<Array[]>`][`<Array>`] arrays with elements to be merged

*Returns:* [`<Array>`]

Distinctly merge multiple arrays


#### mergeObjects(merger, objs)

  - `merger: `[`<Function>`]
  - `objs: `[`<Object[]>`][`<Object>`] objects to be merged

*Returns:* [`<Object>`]

Merge multiple objects with merger


#### Enum()



#### Enum.from()



#### Enum.NaE()



#### Enum.prototype.constructor(valid, hints, compliance)

  - `valid: `[`<boolean>`]
  - `hints: `[`<Object>`]
    - `required: `[`<Array>`]
    - `optional: `[`<Array>`]
  - `compliance: `[`<number>`] ratio of passed optional tests to all optional
        tests

AuthenticationStrength constructor


#### forwardEvents(from, to, events)

  - `from` `<EventEmitter>` to listen for event
  - `to` `<EventEmitter>` to emit event on
  - `events: `[`<string>`]` | `[`<Object>`]` | `[`<string[]>`][`<string>`]
        (optional), events names

Forward events from one EventEmitter to another

*Example:* 
```js
 forwardEvents(from, to);
```

*Example:* 
```js
 forwardEvents(from, to, 'eventName');
```

*Example:* 
```js
 forwardEvents(from, to, { eventName: 'newEventName' });
```

*Example:* 
```js
 forwardEvents(from, to, ['eventName1', 'eventName2']);
```


#### emitter()


*Returns:* `<EventEmitter>`

Create EnhancedEmitter, enhanced EventEmitter

with wildcard and forward method


#### Flags()



#### Flags.from()



#### Flags.prototype.constructor(valid, hints, compliance)

  - `valid: `[`<boolean>`]
  - `hints: `[`<Object>`]
    - `required: `[`<Array>`]
    - `optional: `[`<Array>`]
  - `compliance: `[`<number>`] ratio of passed optional tests to all optional
        tests

AuthenticationStrength constructor


#### partial(fn, args)

  - `fn: `[`<Function>`]
  - `args: `[`<Array>`] arguments to be applied

*Returns:* [`<Function>`]
  - `rest: `[`<Array>`] arguments

Partially apply arguments to function


#### omap(mapFn, obj)

  - `mapFn: `[`<Function>`] to apply to every field value
  - `obj: `[`<Object>`] which fields used for mapping

*Returns:* [`<Object>`] with same reference but with transformed fields

Map object fields with provided function


#### compose(fns)

  - `fns: `[`<Array>`] functions to be composed

*Returns:* [`<Function>`] composed
  - `args: `[`<Array>`] arguments to be passed to the first function

Compose multiple functions into one


#### maybe(fn, defVal, value)

  - `fn: `[`<Function>`]
  - `defVal: <any>` default value
  - `value: <any>` value (optional)

*Returns:* `<any>` result of `fn` or `defVal`

Apply given function to value or default value


#### zip(arrays)

  - `arrays: `[`<Array[]>`][`<Array>`] arrays to be zipped

*Returns:* [`<Array>`] length is minimal of input arrays length, element with
    index i of resulting array is array with elements with index i from input
    array

Zip several arrays into one


#### replicate(count, elem)

  - `count: `[`<number>`] new array length
  - `elem: <any>` value to replicate

*Returns:* [`<Array>`] replicated

Create array of replicated values


#### zipWith(fn, arrays)

  - `fn: `[`<Function>`] for zipping elements with index i
  - `arrays: `[`<Array[]>`][`<Array>`] arrays to be zipped

*Returns:* [`<Array>`] zipped, element with index i of resulting array is result
    of fn called with arguments from arrays

Zip arrays using specific function


#### curryUntil(condition, fn, args)

  - `condition: `[`<Function>`] function(argsI, argsParts) returns boolean
    - `argsI: `[`<Array>`] arguments for i-th currying
    - `argsParts: `[`<Array>`] of args given for currying from first to i-th
          currying
  - `fn: `[`<Function>`] to be curried
  - `args: `[`<Array>`] arguments for fn

*Returns:* [`<Function>`] curried
  - `args: `[`<Array>`] arguments

Curry function until the condition is met


#### curryN(fn, count, args)

  - `fn: `[`<Function>`] to be curried
  - `count: `[`<number>`] of times function should be curried
  - `args: `[`<Array>`] arguments for first currying

*Returns:* [`<Function>`] curried given times count

Curry fn count times, first curry uses args for first currying


#### curryTwice(fn)

  - `fn: `[`<Function>`] to be curried

*Returns:* [`<Function>`] to pass arguments that returns curried fn

Curry function curry with fn


#### curry(fn, param)

  - `fn: `[`<Function>`] to be curried
  - `param: `[`<Array>`] arguments to the function

*Returns:* [`<Function>`] curried

Curry function with given arguments


#### applyArgs(args)

  - `args: `[`<Array>`] arguments to save in closure

*Returns:* [`<Function>`] fn - <Function>, to be applied saved arguments
  - `Returns:: <any>` result of `fn(...args)`

Apply arguments


#### either(fn)

  - `fn: `[`<Function>`] to be called

*Returns:* [`<Function>`] args - <Array>, arguments to iterate
  - `Returns:: <any>` result of `fn(arg)`, where `arg` - first valid element of
        `args`

Get first not errored result of fn

*Throws:* [`<Error>`] if `fn` throws it


#### restLeft(fn)

  - `fn: `[`<Function>`] function(args, ...namedArgs, callback)
    - `args: `[`<Array>`] rest of spreadArgs created by excluding namedArgs
    - `namedArgs: `[`<Array>`] first values of spreadArgs, length is based upon
          interface of fn
    - `callback: `[`<Function>`] callback, last argument of spreadArgs

*Returns:* [`<Function>`]
  - `spreadArgs: `[`<Array>`] arguments to be added

Rest left, transform function


#### generateKey(length, possible)

  - `length: `[`<number>`] key length
  - `possible: `[`<string>`] with possible characters

*Returns:* [`<string>`] key

Generate random key


#### generateGUID()


*Returns:* [`<string>`] GUID

Generate an RFC4122-compliant GUID (UUID v4)


#### generateSID(config)

  - `config: `[`<Object>`] { length, characters, secret }

*Returns:* [`<string>`] SID

Generate random SID

*Deprecated:* this method will be removed in the next major versions. Use
    `generateToken()` instead.


#### crcSID(config, key)

  - `config: `[`<Object>`] { secret }
  - `key: `[`<string>`] SID key

*Returns:* [`<string>`] CRC

Calculate SID CRC

*Deprecated:* this method will be removed in the next major versions. Use
    `crcToken()` instead.


#### validateSID(config, sid)

  - `config: `[`<Object>`] { secret }
  - `sid: `[`<string>`] session id

*Returns:* [`<boolean>`]

Validate SID

*Deprecated:* this method will be removed in the next major versions. Use
    `validateToken()` instead.


#### generateToken(secret, characters, length)

  - `secret: `[`<string>`]
  - `characters: `[`<string>`]
  - `length: `[`<number>`]

*Returns:* [`<string>`] token

Generate random Token


#### crcToken(secret, key)

  - `secret: `[`<string>`]
  - `key: `[`<string>`]

*Returns:* [`<string>`] crc

Calculate Token crc


#### validateToken(secret, token)

  - `secret: `[`<string>`]
  - `token: `[`<string>`]

*Returns:* [`<boolean>`]

Validate Token


#### hash(password, salt)

  - `password: `[`<string>`]
  - `salt: `[`<string>`]

*Returns:* [`<string>`] hash

Calculate hash with salt


#### validateHash(hashValue, password, salt)

  - `hashValue: `[`<string>`]
  - `password: `[`<string>`]
  - `salt: `[`<string>`]

*Returns:* [`<boolean>`]

Validate hash


#### generateStorageKey()


*Returns:* [`<string[]>`][`<string>`] [folder1, folder2, code]

Generate file storage key


#### idToChunks(id)

  - `id: `[`<number>`]

*Returns:* [`<Array>`] minimal length is 2 which contains hex strings with
    length of 4

Convert id to array of hex strings


#### idToPath(id)

  - `id: `[`<number>`]

*Returns:* [`<string>`]

Convert id to file path


#### pathToId(path)

  - `path: `[`<string>`]

*Returns:* [`<number>`]

Convert file path to id


#### Int64()



#### Int64.zero()



#### Int64.one()



#### Int64._conversion()


Convert signed to 2's complement representation and vise versa


#### Int64.add()



#### Int64.sub()



#### Int64.cmp()



#### Int64._division()



#### Int64.div()



#### Int64.mod()



#### Int64.mult()



#### Int64.and()



#### Int64.or()



#### Int64.not()



#### Int64.xor()



#### Int64.shiftRight()



#### Int64.shiftLeft()



#### Int64.prototype.constructor(valid, hints, compliance)

  - `valid: `[`<boolean>`]
  - `hints: `[`<Object>`]
    - `required: `[`<Array>`]
    - `optional: `[`<Array>`]
  - `compliance: `[`<number>`] ratio of passed optional tests to all optional
        tests

AuthenticationStrength constructor


#### Int64.prototype.toInt32()



#### Int64.prototype.toUint32()



#### Int64.prototype.add()



#### Int64.prototype.sub()



#### Int64.prototype.and()



#### Int64.prototype.or()



#### Int64.prototype.not()



#### Int64.prototype.xor()



#### Int64.prototype.shiftRightLogical()



#### Int64.prototype.shiftRightArithmetic()



#### Int64.prototype.shiftRight()



#### Int64.prototype.shiftLeft()



#### Int64.prototype.inc()



#### Int64.prototype.dec()



#### Int64.prototype.toString()



#### Int64.prototype.toJSON()



#### Int64.prototype.toPostgres()



#### Iterator()



#### Iterator.range(start, stop, step)

  - `start: `[`<number>`]
  - `stop: `[`<number>`]
  - `step: `[`<number>`] optional, default value is 1

*Returns:* `<Iterator>`

Create iterator iterating over the range


#### Iterator.prototype.constructor(valid, hints, compliance)

  - `valid: `[`<boolean>`]
  - `hints: `[`<Object>`]
    - `required: `[`<Array>`]
    - `optional: `[`<Array>`]
  - `compliance: `[`<number>`] ratio of passed optional tests to all optional
        tests

AuthenticationStrength constructor


#### Iterator.prototype.next()



#### Iterator.prototype.count()



#### Iterator.prototype.each()



#### Iterator.prototype.forEach()



#### Iterator.prototype.every()



#### Iterator.prototype.find()



#### Iterator.prototype.includes()



#### Iterator.prototype.reduce()



#### Iterator.prototype.some()



#### Iterator.prototype.someCount()



#### Iterator.prototype.collectTo()



#### Iterator.prototype.collectWith()



#### Iterator.prototype.toArray()



#### Iterator.prototype.map()



#### Iterator.prototype.filter()



#### Iterator.prototype.flat()



#### Iterator.prototype.flatMap()



#### Iterator.prototype.zip()



#### Iterator.prototype.chain()



#### Iterator.prototype.take()



#### Iterator.prototype.takeWhile()



#### Iterator.prototype.skip()



#### Iterator.prototype.enumerate()



#### Iterator.prototype.join()



#### iter()



#### cryptoPrefetcher(bufSize, valueSize)

  - `bufSize: `[`<number>`] size in bytes of the buffer to preallocate
  - `valueSize: `[`<number>`] size in bytes of the produced chunks

Create prefetcher to use when crypto.randomBytes is required to generate

multiple same-size values. `bufSize` must be a multiple of `valueSize` for
this to work.


#### random(min, max)

  - `min: `[`<number>`] range start
  - `max: `[`<number>`] range end

*Returns:* [`<number>`]

Generate random integer value in given range


#### cryptoRandom()


*Returns:* [`<number>`]

Generate random number in the range from 0 inclusive up to

but not including 1 (same as Math.random),
using crypto-secure number generator.


#### methods(iface)

  - `iface: `[`<Object>`] to be introspected

*Returns:* [`<string[]>`][`<string>`] method names

List method names


#### properties(iface)

  - `iface: `[`<Object>`] to be introspected

*Returns:* [`<string[]>`][`<string>`] property names

List property names


#### ip2int()



#### ipToInt(ip)

  - `ip: `[`<string>`] IP address, default: '127.0.0.1'

*Returns:* [`<number>`]

Convert IP string to number


#### localIPs()


*Returns:* [`<string[]>`][`<string>`]

Get local network interfaces


#### parseHost(host)

  - `host: `[`<string>`] host or empty string, may contain `:port`

*Returns:* [`<string>`] host without port but not empty

Parse host string


#### inherits()



#### override(obj, fn)

  - `obj: `[`<Object>`] containing method to override
  - `fn: `[`<Function>`] name will be used to find method

Override method: save old to `fn.inherited`

Previous function will be accessible by obj.fnName.inherited


#### mixin(target, source)

  - `target: `[`<Object>`] mixin to target
  - `source: `[`<Object>`] source methods

Mixin for ES6 classes without overriding existing methods


#### sortComparePriority(priority, s1, s2)

  - `priority: `[`<string[]>`][`<string>`] with priority
  - `s1: `[`<string>`] to compare
  - `s2: `[`<string>`] to compare

*Returns:* [`<number>`]

Compare for array.sort with priority

*Example:* 
```js
 files.sort(common.sortComparePriority)
```


#### sortCompareDirectories(a, b)

  - `a: `[`<string>`] to compare
  - `b: `[`<string>`] to compare

*Returns:* [`<number>`]

Compare for array.sort, directories first

*Example:* 
```js
 files.sort(sortCompareDirectories);
```


#### sortCompareByName(a, b)

  - `a: `[`<Object>`] { name } to compare
  - `b: `[`<Object>`] { name } to compare

*Returns:* [`<number>`]

Compare for array.sort

*Example:* 
```js
 files.sort(sortCompareByName)
```


#### subst(tpl, data, dataPath, escapeHtml)

  - `tpl: `[`<string>`] template body
  - `data: `[`<Object>`] hash, data structure to visualize
  - `dataPath: `[`<string>`] current position in data structure
  - `escapeHtml: `[`<boolean>`] escape html special characters if true

*Returns:* [`<string>`]

Substitute variables


#### htmlEscape(content)

  - `content: `[`<string>`] to escape

*Returns:* [`<string>`]

Escape html characters

*Example:* 
```js
 htmlEscape('5>=5') = '5&lt;=5'
```


#### fileExt(fileName)

  - `fileName: `[`<string>`] file name

*Returns:* [`<string>`]

Extract file extension in lower case without dot

*Example:* 
```js
 fileExt('/dir/file.txt')
```

*Result:* 
```js
 'txt'
```


#### removeExt(fileName)

  - `fileName: `[`<string>`] file name

*Returns:* [`<string>`]

Remove file extension from file name

*Example:* 
```js
 fileExt('file.txt')
```

*Result:* 
```js
 'file'
```


#### spinalToCamel(name)

  - `name: `[`<string>`]

*Returns:* [`<string>`]

Convert spinal case to camel case


#### escapeRegExp(s)

  - `s: `[`<string>`]

*Returns:* [`<string>`]

Escape regular expression control characters

*Example:* 
```js
 escapeRegExp('/path/to/res?search=this.that')
```


#### newEscapedRegExp(s)

  - `s: `[`<string>`]

*Returns:* [`<RegExp>`]

Generate escaped regular expression


#### addTrailingSlash(s)

  - `s: `[`<string>`]

*Returns:* [`<string>`]

Add trailing slash at the end if there isn't one


#### stripTrailingSlash(s)

  - `s: `[`<string>`]

*Returns:* [`<string>`]

Remove trailing slash from string


#### dirname(filePath)

  - `filePath: `[`<string>`]

*Returns:* [`<string>`]

Get directory name with trailing slash from path


#### capitalize(s)

  - `s: `[`<string>`]

*Returns:* [`<string>`]

Capitalize string


#### between(s, prefix, suffix)

  - `s: `[`<string>`] source
  - `prefix: `[`<string>`] before needed fragment
  - `suffix: `[`<string>`] after needed fragment

*Returns:* [`<string>`]

Extract substring between prefix and suffix


#### removeBOM(s)

  - `s: `[`<string>`] possibly starts with BOM

*Returns:* [`<string>`]

Remove UTF-8 BOM


#### arrayRegExp(items)

  - `items: `[`<string[]>`][`<string>`]

*Returns:* [`<RegExp>`]

Generate RegExp from array with '*' wildcards

*Example:* 
```js
 ['/css/*', '/index.html']
```


#### section(s, separator)

  - `s: `[`<string>`]
  - `separator: `[`<string>`] or char

*Returns:* [`<string[]>`][`<string>`]

Split string by the first occurrence of separator

*Example:* 
```js
 rsection('All you need is JavaScript', 'is')
```

*Result:* 
```js
 ['All you need ', ' JavaScript']
```


#### rsection(s, separator)

  - `s: `[`<string>`]
  - `separator: `[`<string>`] or char

*Returns:* [`<string[]>`][`<string>`]

Split string by the last occurrence of separator

*Example:* 
```js
 rsection('All you need is JavaScript', 'a')
```

*Result:* 
```js
 ['All you need is Jav', 'Script']
```


#### split(s, separator, limit)

  - `s: `[`<string>`]
  - `separator: `[`<string>`] (optional), default: ','
  - `limit: `[`<number>`] (optional), default: -1 max length of result array

*Returns:* [`<string[]>`][`<string>`]

Split string by multiple occurrence of separator

*Example:* 
```js
 split('a,b,c,d')
```

*Result:* 
```js
 ['a', 'b', 'c', 'd']
```

*Example:* 
```js
 split('a,b,c,d', ',', 2)
```

*Result:* 
```js
 ['a', 'b']
```


#### rsplit(s, separator, limit)

  - `s: `[`<string>`]
  - `separator: `[`<string>`] (optional), default: ','
  - `limit: `[`<number>`] (optional), default: -1 max length of result array

*Returns:* [`<string[]>`][`<string>`]

Split string by multiple occurrences of separator

*Example:* 
```js
 split('a,b,c,d', ',', 2)
```

*Result:* 
```js
 ['c', 'd']
```


#### normalizeEmail(email)

  - `email: `[`<string>`] email address to normalize

*Returns:* [`<string>`] normalized email address

Normalize email address according to OWASP recommendations


#### isTimeEqual(time1, time2)

  - `time1: `[`<string>`] time or milliseconds
  - `time2: `[`<string>`] time or milliseconds

*Returns:* [`<boolean>`]

Compare time1 and time2

*Example:* 
```js
 isTimeEqual(sinceTime, buffer.stats.mtime)
```


#### nowDate(date)

  - `date: `[`<Date>`] (optional), default: new Date()

*Returns:* [`<string>`]

Get current date in YYYY-MM-DD format


#### nowDateTime(date)

  - `date: `[`<Date>`] (optional), default: new Date()

*Returns:* [`<string>`]

Get current date in YYYY-MM-DD hh:mm format


#### Uint64()



#### Uint64.add()



#### Uint64.sub()



#### Uint64.mult()



#### Uint64.cmp()



#### Uint64._division()



#### Uint64.div()



#### Uint64.mod()



#### Uint64.and()



#### Uint64.or()



#### Uint64.not()



#### Uint64.xor()



#### Uint64.shiftRight()



#### Uint64.shiftLeft()



#### Uint64.prototype.constructor(valid, hints, compliance)

  - `valid: `[`<boolean>`]
  - `hints: `[`<Object>`]
    - `required: `[`<Array>`]
    - `optional: `[`<Array>`]
  - `compliance: `[`<number>`] ratio of passed optional tests to all optional
        tests

AuthenticationStrength constructor


#### Uint64.prototype.toUint32()



#### Uint64.prototype.add()



#### Uint64.prototype.sub()



#### Uint64.prototype.and()



#### Uint64.prototype.or()



#### Uint64.prototype.not()



#### Uint64.prototype.xor()



#### Uint64.prototype.shiftRight()



#### Uint64.prototype.shiftLeft()



#### Uint64.prototype.inc()



#### Uint64.prototype.dec()



#### Uint64.prototype.toString()



#### Uint64.prototype.toJSON()



#### Uint64.prototype.toPostgres()



#### duration(s)

  - `s: `[`<string>`] duration syntax

*Returns:* [`<number>`] milliseconds

Parse duration to seconds

*Example:* 
```js
 duration('1d 10h 7m 13s')
```


#### durationToString(n)

  - `n: `[`<number>`] duration

*Returns:* [`<string>`]

Convert integer duration to string


#### bytesToSize(bytes)

  - `bytes: `[`<number>`] size

*Returns:* [`<string>`]

Convert integer to string, representing data size in Kb, Mb, Gb, and Tb


#### sizeToBytes(size)

  - `size: `[`<string>`] size

*Returns:* [`<number>`]

Convert string with data size to integer


#### deprecate(fn)

  - `fn: `[`<Function>`]

*Returns:* [`<Function>`] wrapped with deprecation warning
  - `args: `[`<Array>`] arguments to be passed to wrapped function

Wrap method to mark it as deprecated


#### alias(fn)

  - `fn: `[`<Function>`]

*Returns:* [`<Function>`] wrapped with deprecation warning
  - `args: `[`<Array>`] arguments to be passed to wrapped function

Wrap new method to mark old alias as deprecated


#### safe(fn)

  - `fn: `[`<Function>`]

*Returns:* [`<Function>`] wrapped with try/catch interception
  - `args: `[`<Array>`] arguments to be passed to wrapped function

Make function raise-safe


#### callerFilename()



#### callerFilepath()



[`<Object>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object
[`<Date>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date
[`<Function>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function
[`<RegExp>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp
[`<DataView>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/DataView
[`<Map>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map
[`<WeakMap>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap
[`<Set>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set
[`<WeakSet>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet
[`<Array>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array
[`<ArrayBuffer>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer
[`<Int8Array>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Int8Array
[`<Uint8Array>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array
[`<Uint8ClampedArray>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8ClampedArray
[`<Int16Array>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Int16Array
[`<Uint16Array>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint16Array
[`<Int32Array>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Int32Array
[`<Uint32Array>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint32Array
[`<Float32Array>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Float32Array
[`<Float64Array>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Float64Array
[`<Error>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error
[`<EvalError>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/EvalError
[`<TypeError>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError
[`<RangeError>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RangeError
[`<SyntaxError>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError
[`<ReferenceError>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ReferenceError
[`<boolean>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#Boolean_type
[`<null>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#Null_type
[`<undefined>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#Undefined_type
[`<number>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#Number_type
[`<string>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#String_type
[`<symbol>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#Symbol_type
[`<Primitive>`]: https://developer.mozilla.org/en-US/docs/Glossary/Primitive
[`<Iterable>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols
[`<this>`]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this