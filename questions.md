# JavaScript Architect Roadmap — Complete Interview & Study Questions

> An exhaustive, architect-level question bank covering JavaScript language internals, asynchronous programming, advanced patterns, security, reliability, performance, browser APIs, tooling, and server-side JavaScript.

---

## 1. Core Language Deep Dive

### Language Fundamentals

- What is JavaScript, and what are its core characteristics?
- How is JavaScript different from Java?
- Is JavaScript interpreted, compiled, or both?
- What is ECMAScript?
- What is the relationship between JavaScript and ECMAScript?
- What are the major ECMAScript language editions?
- What are the differences between scripting languages and compiled languages?
- What are the execution phases of a JavaScript program?
- What is the difference between source code, bytecode, and machine code?
- What is JIT compilation?
- How does a modern JavaScript engine execute code?
- What are the major components of a JavaScript engine?
- What are the differences between V8, SpiderMonkey, and JavaScriptCore?
- What is strict mode?
- Why was strict mode introduced?
- How do you enable strict mode?
- What changes when strict mode is enabled?
- What are the restrictions imposed by strict mode?
- What is sloppy mode?
- Why should production code generally use strict mode or ES modules?
- What are statements and expressions?
- What is the difference between an expression and a declaration?
- What is an expression statement?
- What is automatic semicolon insertion?
- What are the rules of automatic semicolon insertion?
- What are common bugs caused by automatic semicolon insertion?
- When should semicolons be used explicitly?
- What are reserved words in JavaScript?
- What are contextual keywords?
- What are identifiers?
- What are valid and invalid JavaScript identifiers?
- What is Unicode support in JavaScript identifiers?
- What is the difference between comments and executable code?
- What are single-line, multi-line, and hashbang comments?
- What is the purpose of a hashbang in Node.js scripts?

### Variables, Scope, and Bindings

- What is the difference between `var`, `let`, and `const`?
- What is function scope?
- What is block scope?
- What is module scope?
- What is global scope?
- What is lexical scope?
- What is dynamic scope?
- Does JavaScript use lexical or dynamic scoping?
- What is the scope chain?
- How is a variable resolved through the scope chain?
- What is a binding?
- What is the difference between declaring and initializing a variable?
- What is the temporal dead zone?
- Why does the temporal dead zone exist?
- What happens when a `let` or `const` variable is accessed before initialization?
- Can a `const` object be mutated?
- Can a `const` variable be reassigned?
- What is variable shadowing?
- What is illegal shadowing?
- What happens when a local variable has the same name as a global variable?
- What is hoisting?
- Which declarations are hoisted?
- Are `let` and `const` hoisted?
- Are function declarations hoisted?
- How are function declarations and function expressions hoisted differently?
- What is the difference between declaration hoisting and initialization?
- What is the global object?
- What is the global environment record?
- What is the difference between a global `var` and a global `let`?
- Why does a top-level `let` not become a property of `window`?
- What is the `globalThis` object?
- How does `globalThis` work across browsers and Node.js?
- What is variable masking?
- What is scope pollution?
- How can accidental globals be created?
- How can accidental globals be prevented?
- What are best practices for variable naming and scope design?

### Data Types and Values

- What are JavaScript's primitive data types?
- What are JavaScript's non-primitive/reference types?
- What is the difference between primitive and reference values?
- What is the difference between `undefined` and `null`?
- Why does `typeof null` return `"object"`?
- What does `typeof` return for every JavaScript type?
- What is the `typeof` operator unable to distinguish?
- What is `Symbol`?
- Why was `Symbol` introduced?
- What are well-known symbols?
- What is `BigInt`?
- When should `BigInt` be used?
- What are the limitations of `BigInt`?
- Can `BigInt` and `Number` be mixed in arithmetic?
- What is `NaN`?
- Why is `NaN !== NaN`?
- How can `NaN` be detected reliably?
- What is the difference between `isNaN()` and `Number.isNaN()`?
- What is positive zero?
- What is negative zero?
- How can negative zero be detected?
- What is the difference between `Object.is()` and `===`?
- What are boxed primitives?
- What happens when a primitive value accesses a method?
- What is autoboxing?
- What is type coercion?
- What is implicit coercion?
- What is explicit coercion?
- What are truthy and falsy values?
- List all falsy values in JavaScript.
- Why is an empty array truthy?
- Why is an empty object truthy?
- What is the difference between equality and identity?
- What is the difference between `==` and `===`?
- What are the abstract equality comparison rules?
- What are the strict equality comparison rules?
- What are the relational comparison rules?
- What is the difference between `Object.is`, `===`, and `==`?
- What is type narrowing in JavaScript?
- How do JavaScript values behave in Boolean contexts?
- What are safe ways to validate unknown values?
- How can runtime type checks be designed robustly?

### Numbers, Strings, and Conversion

- How are numbers represented internally in JavaScript?
- What is IEEE 754 double-precision floating point?
- What is the safe integer range in JavaScript?
- What are `Number.MAX_SAFE_INTEGER` and `Number.MIN_SAFE_INTEGER`?
- What are floating-point precision errors?
- Why does `0.1 + 0.2` not exactly equal `0.3`?
- How should monetary values be represented?
- When should decimal libraries or integer minor units be used?
- What are `Number.EPSILON` and `Number.isFinite()`?
- What is the difference between `parseInt`, `parseFloat`, and `Number`?
- Why should the radix be supplied to `parseInt`?
- How does numeric string conversion work?
- What is the difference between `String(value)` and `value.toString()`?
- What happens when converting `null` and `undefined` to strings?
- What are template literals?
- What are tagged template literals?
- How do escape sequences work?
- What is the difference between UTF-16 code units and Unicode code points?
- What is a surrogate pair?
- What are Unicode grapheme clusters?
- Why can `string.length` be different from the number of visible characters?
- What is the difference between `charAt`, `charCodeAt`, `codePointAt`, and `at`?
- How do `for...of` and string iteration handle Unicode?
- What are normalization forms such as NFC and NFD?
- Why is Unicode normalization important?
- How should internationalized string comparisons be performed?
- What is `Intl.Collator`?
- What is `Intl.NumberFormat`?
- What is `Intl.DateTimeFormat`?
- What is `Intl.RelativeTimeFormat`?
- What is `Intl.Segmenter`?
- How should locale-sensitive formatting be architected?

### Operators and Expressions

- What are unary, binary, and ternary operators?
- What is operator precedence?
- What is operator associativity?
- How does short-circuit evaluation work?
- What is the difference between `||` and `??`?
- When should nullish coalescing be preferred over logical OR?
- What is optional chaining?
- How does optional chaining short-circuit?
- What is the difference between `?.`, `&&`, and explicit null checks?
- What are logical assignment operators?
- What is the difference between `||=`, `&&=`, and `??=`?
- What is the comma operator?
- What is the `void` operator?
- What is the `delete` operator?
- What is the `in` operator?
- What is the `instanceof` operator?
- What is the difference between `in` and `Object.hasOwn()`?
- What is the exponentiation operator?
- What is the difference between prefix and postfix increment?
- What are bitwise operators used for?
- What are the risks of using bitwise operators with large numbers?
- What is the conditional operator?
- How can complex expressions harm readability?
- What are best practices for operator-heavy code?

### Functions

- What is a function in JavaScript?
- What are function declarations, function expressions, and arrow functions?
- What are named and anonymous functions?
- What are first-class functions?
- What is a higher-order function?
- What is a callback function?
- What is a pure function?
- What is an impure function?
- What is function composition?
- What is currying?
- What is partial application?
- What is memoization?
- What is recursion?
- What is tail recursion?
- Does JavaScript guarantee proper tail calls?
- What is the call stack?
- What causes stack overflow?
- What is the difference between a function parameter and an argument?
- What are default parameters?
- What are rest parameters?
- What is the `arguments` object?
- How does `arguments` differ from rest parameters?
- Why do arrow functions not have their own `arguments` object?
- What are spread arguments?
- What is the difference between spread syntax and rest syntax?
- What are function return values?
- What happens when a function does not explicitly return?
- What is a callback convention?
- What is callback hell?
- How can callback-based APIs be designed cleanly?
- What is a function's `length` property?
- What is a function's `name` property?
- What is the difference between callable and constructable functions?
- What are generator functions?
- What are async functions?
- What are methods and accessors?
- What are function constructors?
- What is the difference between a function and a class?
- How should functions be kept small and cohesive?
- How should function side effects be documented?

### Closures and Lexical Environment

- What is a closure?
- How is a closure created?
- What is a lexical environment?
- What is an environment record?
- How does a closure retain access to outer variables?
- Why do closures not necessarily retain every variable in an outer function?
- What are practical uses of closures?
- How can closures implement private state?
- How can closures implement factories?
- How can closures implement memoization?
- How can closures implement module patterns?
- What are common closure-related memory leaks?
- How do closures behave inside loops?
- Why does `var` behave differently from `let` in loops with callbacks?
- How can an IIFE solve older closure problems?
- What are closure performance considerations?
- How can closure-heavy code be debugged?
- What is the difference between lexical scope and closure?
- How do closures interact with asynchronous callbacks?
- How do closures interact with event listeners?
- How can closures accidentally retain large objects?
- How can closure lifetime be controlled?

### Objects and Prototypes

- What is an object in JavaScript?
- How are objects created?
- What is an object literal?
- What is the prototype chain?
- What is `Object.prototype`?
- What is the difference between `__proto__` and `prototype`?
- What does `Object.create()` do?
- What is prototypal inheritance?
- How does property lookup work?
- How does method lookup work?
- What happens when a property is missing?
- What is property shadowing?
- What are own properties and inherited properties?
- What is the difference between enumerable, configurable, and writable?
- What are property descriptors?
- How do `Object.defineProperty()` and `Object.defineProperties()` work?
- What are accessor properties?
- What are data properties?
- What is the difference between getters and methods?
- What is object mutability?
- What is object extensibility?
- What do `Object.preventExtensions`, `Object.seal`, and `Object.freeze` do?
- Are `Object.freeze()` and `Object.seal()` deep operations?
- How can deep immutability be implemented?
- What is the difference between shallow copy and deep copy?
- What are safe ways to clone objects?
- What are the limitations of `JSON.parse(JSON.stringify())` cloning?
- What does `structuredClone()` support?
- What are property keys?
- Can object keys be objects?
- How are object keys converted?
- What is the difference between dot notation and bracket notation?
- What are computed property names?
- What is object shorthand syntax?
- What are method definitions?
- What is object destructuring?
- What are nested destructuring patterns?
- How do default values work in destructuring?
- What is the difference between object spread and `Object.assign()`?
- How do symbols behave as object keys?
- What is property order in JavaScript objects?
- What are null-prototype objects?
- When should null-prototype objects be used?
- What are risks of prototype pollution?
- How can objects be safely used as dictionaries?
- What is the difference between `hasOwnProperty` and `Object.hasOwn`?
- What are proxy objects?
- What are reflective operations?
- How should domain objects be modeled?

### Classes and Inheritance

- What are JavaScript classes?
- Are JavaScript classes syntactic sugar over prototypes?
- What is a class constructor?
- What happens when a class is instantiated?
- What is the difference between instance methods and static methods?
- What are public fields?
- What are private class fields?
- What are private methods?
- What are static initialization blocks?
- What is class inheritance?
- What does `extends` do?
- What does `super` do?
- How does constructor chaining work?
- What happens when a derived constructor does not call `super()`?
- What is method overriding?
- What is polymorphism?
- What is encapsulation in JavaScript classes?
- What are abstract classes, and how can they be simulated?
- What are mixins?
- What are composition and inheritance trade-offs?
- When should inheritance be avoided?
- How do private fields differ from naming conventions such as `_private`?
- How do class fields affect `this` binding?
- What are static blocks useful for?
- How do classes interact with decorators?
- What are common class design mistakes?
- How should classes be tested?
- How should class hierarchies be kept maintainable?

### Arrays, Collections, and Iteration

- What is an array?
- Are JavaScript arrays true arrays?
- How are arrays represented internally by engines?
- What are dense and sparse arrays?
- What happens when an array index is skipped?
- What is the `length` property of an array?
- How do `push`, `pop`, `shift`, and `unshift` work?
- What is the difference between `slice` and `splice`?
- What is the difference between `map`, `forEach`, `filter`, and `reduce`?
- What is the difference between `find`, `findIndex`, `findLast`, and `findLastIndex`?
- What is the difference between `some` and `every`?
- What are `flat` and `flatMap`?
- What is the difference between `includes` and `indexOf`?
- How does `sort` work?
- Why should a comparator be supplied to `sort`?
- Is `sort` stable?
- What is the difference between `toSorted` and `sort`?
- What are `toReversed`, `toSpliced`, and `with`?
- What is array destructuring?
- What is array spread?
- How can arrays be copied safely?
- What are typed arrays?
- What is `ArrayBuffer`?
- What is `DataView`?
- What is a `Uint8Array`?
- What is a `SharedArrayBuffer`?
- What is a `Map`?
- When should `Map` be used instead of an object?
- What is a `Set`?
- How does `Set` determine uniqueness?
- What are `WeakMap` and `WeakSet`?
- Why are weak collections not iterable?
- What is an iterator?
- What is an iterable?
- What is the iterator protocol?
- What is the iterable protocol?
- What is the difference between `for...in` and `for...of`?
- How do custom iterables work?
- What are generator iterators?
- How can collection operations be made lazy?
- What are the performance characteristics of arrays, maps, and sets?
- How should large collections be processed efficiently?

### Iterators and Generators

- What is a generator function?
- What does `yield` do?
- What does `yield*` do?
- What does a generator return?
- How does `next()` work?
- What do `return()` and `throw()` do on generators?
- How can values be passed into a generator?
- How can generators model state machines?
- How can generators implement lazy sequences?
- How can generators support pagination?
- How can generators be used for streaming data?
- What is the difference between synchronous and asynchronous generators?
- What is `for await...of`?
- How do generators interact with promises?
- What are generator cancellation patterns?
- What are generator performance trade-offs?
- When should generators not be used?

### Errors and Exceptions

- What is an exception?
- What is the difference between an error and an exception?
- What are built-in error types?
- What is the difference between `Error`, `TypeError`, `ReferenceError`, and `SyntaxError`?
- What are `RangeError`, `URIError`, and `EvalError`?
- How do `try`, `catch`, and `finally` work?
- Does `finally` always execute?
- What happens when `finally` returns a value?
- How should errors be thrown?
- Why should errors generally be instances of `Error`?
- What is error chaining?
- What is the `cause` property?
- What are custom error classes?
- How should errors be serialized?
- How should errors be logged?
- What is the difference between operational and programmer errors?
- How should errors cross asynchronous boundaries?
- What is an unhandled promise rejection?
- What is an uncaught exception?
- How should an application recover from errors?
- When should an error be retried?
- When should an error be allowed to fail fast?
- How should error messages avoid leaking sensitive information?
- How should errors be represented in APIs?
- How should error handling be tested?

### Modules and Code Organization

- What are JavaScript modules?
- What is the difference between ES modules and CommonJS?
- What is the module resolution process?
- What are named exports?
- What are default exports?
- What are namespace imports?
- What are re-exports?
- What is a barrel file?
- What are live bindings?
- What is module scope?
- How does module strict mode work?
- What is top-level `await`?
- What is a circular dependency?
- How do circular dependencies behave in ES modules?
- How do circular dependencies behave in CommonJS?
- What is tree shaking?
- What makes code tree-shakeable?
- What are side-effectful modules?
- What is the `sideEffects` package field?
- What are dynamic imports?
- How do modules load in browsers?
- How do modules load in Node.js?
- What is import maps?
- What are import assertions and import attributes?
- What are module workers?
- What is module preloading?
- How should modules be organized in a large application?
- How should public and private module APIs be designed?
- How can module boundaries reduce coupling?
- How should circular dependencies be prevented?
- How should modules be tested independently?

### Metaprogramming, Proxies, and Reflection

- What is metaprogramming?
- What is a `Proxy`?
- What is a proxy target?
- What are proxy traps?
- What is the `Reflect` API?
- How do `Proxy` and `Reflect` work together?
- What are proxy invariants?
- How can proxies implement validation?
- How can proxies implement logging?
- How can proxies implement reactivity?
- How can proxies implement access control?
- What are proxy performance costs?
- What are proxy debugging challenges?
- What is `Reflect.get`?
- What is `Reflect.set`?
- What is `Reflect.construct`?
- What is `Reflect.ownKeys`?
- What is `Reflect.defineProperty`?
- What is `Reflect.preventExtensions`?
- What are symbols used for in metaprogramming?
- What are custom `toStringTag` values?
- What are iterators and async iterators as metaprogramming interfaces?
- When should proxies be avoided?

### Regular Expressions

- What is a regular expression?
- What are regex literals and constructor syntax?
- What are regex flags?
- What are capturing groups?
- What are non-capturing groups?
- What are named capture groups?
- What are lookaheads and lookbehinds?
- What are backreferences?
- What is greedy versus lazy matching?
- What is the difference between `g`, `y`, and `u` flags?
- What does the `s` flag do?
- What does the `d` flag do?
- What is Unicode-aware regex matching?
- What is catastrophic backtracking?
- How can regex denial-of-service attacks happen?
- How can regex patterns be made safe?
- When should regex be replaced with a parser?
- How should regexes be tested?
- What are common regex maintainability problems?

### Date, Time, and Internationalization

- Why is the legacy `Date` API difficult to use?
- How are JavaScript dates represented?
- What is the difference between local time and UTC?
- What is an ISO 8601 timestamp?
- What is the difference between a timestamp and a calendar date?
- What are daylight saving time issues?
- Why can date parsing vary across environments?
- What is the difference between `Date.now()` and `new Date()`?
- How can time zones be handled safely?
- What is the Temporal proposal?
- What are `Temporal.Instant`, `Temporal.PlainDate`, and `Temporal.ZonedDateTime`?
- How should date-only values be stored?
- How should recurring events be modeled?
- How should time be tested deterministically?
- What are internationalization APIs?
- How should locale and time-zone preferences be managed?
- What are best practices for date formatting in enterprise applications?

### JavaScript Engine Internals

- What is an execution context?
- What are global, function, and eval execution contexts?
- What is the execution context stack?
- What is the environment record?
- What is the realm?
- What is the job queue?
- What is the heap?
- What is the stack?
- What is garbage collection?
- What are mark-and-sweep and generational garbage collection?
- What are hidden classes?
- What are shapes or object maps?
- What are inline caches?
- What is monomorphic code?
- What is polymorphic code?
- What is megamorphic code?
- What is deoptimization?
- What causes JIT deoptimization?
- How do object property layouts affect performance?
- Why can changing object shapes harm performance?
- What are packed and holey arrays?
- What is escape analysis?
- How do engines optimize closures?
- What are engine warm-up effects?
- How can engine internals be investigated safely?
- Which engine optimizations should developers avoid relying on?
- How do JavaScript engine differences affect portability?

---

## 2. Asynchronous Mastery

### Asynchronous Fundamentals

- What is synchronous execution?
- What is asynchronous execution?
- What is concurrency?
- What is parallelism?
- What is the difference between concurrency and parallelism?
- Why is JavaScript often described as single-threaded?
- What does single-threaded mean in the browser?
- Can JavaScript execute work in parallel?
- What is the event loop?
- What is the call stack?
- What is the task queue?
- What is the microtask queue?
- What is the event loop's execution order?
- What is a macrotask?
- What is a microtask?
- What are rendering opportunities in the browser event loop?
- What is the difference between browser and Node.js event loops?
- What is the role of the host environment?
- What work is handled by the JavaScript engine versus the host?
- What is cooperative scheduling?
- What is blocking code?
- What is non-blocking code?
- What is starvation?
- What is event-loop lag?
- How can event-loop lag be measured?
- What is reentrancy?
- What are race conditions in JavaScript?
- What are timing-dependent bugs?
- How can asynchronous code be made deterministic?

### Callbacks

- What is a callback?
- What is callback-based asynchronous programming?
- What is callback hell?
- What are error-first callbacks?
- Why are error-first callbacks common in Node.js?
- What is inversion of control?
- What are callback contracts?
- What happens if a callback is called twice?
- What happens if a callback is never called?
- How can callback APIs enforce exactly-once completion?
- How can callback APIs be converted into promises?
- What are callback cancellation patterns?
- What is callback context?
- How does `this` behave in callbacks?
- What are callback memory leaks?
- How can callback nesting be reduced?
- When are callbacks still preferable to promises?

### Promises

- What is a promise?
- What are the states of a promise?
- What is the difference between pending, fulfilled, and rejected?
- Can a promise change state more than once?
- What is promise settlement?
- What is promise resolution?
- What is the difference between resolved and fulfilled?
- What is promise assimilation?
- What is a thenable?
- How does `Promise.resolve()` work?
- How does `Promise.reject()` work?
- What is promise chaining?
- How does `.then()` return a new promise?
- How does `.catch()` work?
- How does `.finally()` work?
- How are errors propagated through a promise chain?
- What happens when a `.then()` callback throws?
- What happens when a `.then()` callback returns a promise?
- What happens when a `.then()` callback returns a thenable?
- What is the difference between returning and awaiting a promise?
- What happens when a promise rejection is not handled?
- What is an unhandled rejection?
- How can unhandled rejections be monitored?
- What are promise anti-patterns?
- What is the promise constructor anti-pattern?
- What is the difference between `new Promise` and `Promise.resolve`?
- How can promises be cancelled?
- Why do promises not have native cancellation?
- How does `AbortController` work with promises?
- How can promise timeouts be implemented?
- How can retries be implemented with promises?
- How can promise concurrency be limited?
- How can promise results be cached?
- How can promise chains be debugged?
- What are promise memory considerations?

### Promise Combinators

- What does `Promise.all()` do?
- What happens when one promise passed to `Promise.all()` rejects?
- Does `Promise.all()` cancel remaining operations?
- Does `Promise.all()` preserve input order?
- What happens when `Promise.all()` receives non-promises?
- What does `Promise.allSettled()` do?
- When should `Promise.allSettled()` be used?
- What does `Promise.race()` do?
- How can `Promise.race()` implement a timeout?
- What does `Promise.any()` do?
- What is `AggregateError`?
- What is the difference between `Promise.any()` and `Promise.race()`?
- What does `Promise.withResolvers()` provide?
- How should promise combinators be selected?
- How can partial success be handled?
- How can failures be aggregated meaningfully?
- How can a batch of asynchronous tasks be made resilient?

### Async/Await

- What is `async`?
- What does an async function return?
- What is the difference between `await` and `.then()`?
- What happens when `await` receives a non-promise?
- How does `await` affect execution?
- Does `await` block the JavaScript thread?
- What is the relationship between `await` and microtasks?
- How are errors handled in async functions?
- What happens when an async function throws?
- What is the difference between sequential and parallel `await`?
- Why can sequential awaits reduce performance?
- How should independent async operations be started?
- What is the best way to use `Promise.all()` with async functions?
- What are common async/await anti-patterns?
- How can async functions be cancelled?
- How can async functions be timed out?
- How can async functions be retried?
- How can async functions be tested?
- What is top-level `await`?
- What are the risks of top-level `await`?
- How does async/await work with transactions?
- How can async context be preserved?
- How can async functions avoid hidden race conditions?

### Event Loop and Scheduling

- Explain the complete browser event loop.
- Explain the complete Node.js event loop.
- What is the order of synchronous code, microtasks, timers, and rendering?
- Why do promise callbacks run before timer callbacks?
- What is the difference between `queueMicrotask()` and `setTimeout(..., 0)`?
- What is the difference between `setTimeout` and `setInterval`?
- What is `setImmediate` in Node.js?
- What is `process.nextTick()`?
- Why can `process.nextTick()` starve the event loop?
- What is `MessageChannel`?
- What is `postMessage` scheduling?
- What is `requestAnimationFrame`?
- What is `requestIdleCallback`?
- What is the scheduler API?
- What is cooperative yielding?
- How can long tasks be split into smaller tasks?
- What is the Long Tasks API?
- What is a task source?
- What is timer clamping?
- Why are browser timers not precise?
- What are background-tab timer restrictions?
- How do nested timers behave?
- What is event-loop starvation?
- How can a microtask loop freeze an application?
- How can rendering be blocked by JavaScript?
- How should CPU-heavy work be scheduled?
- How can task priorities be modeled?

### Cancellation, Timeouts, and Retries

- Why is cancellation important in asynchronous systems?
- What is `AbortController`?
- What is `AbortSignal`?
- How does `AbortSignal.timeout()` work?
- How does `AbortSignal.any()` work?
- How can fetch requests be cancelled?
- How can multiple operations share one abort signal?
- How should cancellation errors be represented?
- What is cooperative cancellation?
- What is the difference between cancellation and timeout?
- How can a timeout wrapper be implemented?
- What is retry with exponential backoff?
- What is jitter?
- Why is jitter important in distributed systems?
- What is a retry budget?
- What is a maximum retry limit?
- Which errors should not be retried?
- What is idempotency?
- How does retry interact with non-idempotent operations?
- What is a circuit breaker?
- What is a bulkhead pattern?
- What is hedged execution?
- How can cancellation be propagated through nested operations?
- How can abandoned async work cause memory leaks?
- How should cancellation be tested?

### Concurrency Control

- What is uncontrolled concurrency?
- What is a concurrency limit?
- How can a promise pool be implemented?
- How can a semaphore be implemented in JavaScript?
- How can a mutex be implemented?
- What is a queue-based concurrency limiter?
- What is backpressure?
- How can backpressure be implemented for async iterables?
- What is a worker pool?
- How can requests be deduplicated?
- What is request coalescing?
- What is a single-flight pattern?
- How can duplicate API requests be prevented?
- How can rate limiting be implemented on the client?
- What is token-bucket rate limiting?
- What is leaky-bucket rate limiting?
- How can concurrency limits be tuned?
- How can fairness be maintained?
- What is starvation in a concurrency limiter?
- How can priority queues be implemented?
- How can asynchronous locks be safely released?
- What happens when a task fails while holding a lock?
- How can deadlocks be avoided?
- How can concurrent state updates be serialized?
- How can optimistic concurrency be implemented?

### Async Iteration and Streams

- What is an async iterable?
- What is an async iterator?
- What is `Symbol.asyncIterator`?
- What is `for await...of`?
- How do async generators work?
- How can async generators wrap paginated APIs?
- How can async generators consume streams?
- How can async generators implement polling?
- How can async iterators be cancelled?
- What is a Web Stream?
- What is a readable stream?
- What is a writable stream?
- What is a transform stream?
- What is a `ReadableStream`?
- What is a `WritableStream`?
- What is a `TransformStream`?
- What is a stream controller?
- What is a stream reader?
- What is a stream writer?
- What is backpressure in Web Streams?
- What is a BYOB reader?
- What is stream teeing?
- How can streams be piped?
- What is `pipeThrough`?
- What is `pipeTo`?
- How can stream errors be handled?
- How can streams be cancelled?
- How can streams be converted to async iterables?
- How can streams be consumed without buffering everything?
- What are stream performance considerations?

### Reactive and Event-Driven Programming

- What is event-driven architecture?
- What is reactive programming?
- What is the difference between events, promises, and observables?
- What is an observable?
- What are cold and hot observables?
- What is subscription?
- What is unsubscription?
- What is backpressure in reactive systems?
- What is event composition?
- What is event transformation?
- What is event filtering?
- What is event debouncing?
- What is event throttling?
- What is buffering?
- What is sampling?
- What is switch-to-latest behavior?
- What is event replay?
- What is event sourcing?
- What are event buses?
- What are the risks of global event buses?
- How can event listeners be cleaned up?
- How can event-driven systems be debugged?
- How can event ordering be guaranteed?
- How can duplicate events be handled?
- How can event handlers be made idempotent?

---

## 3. Advanced Patterns

### Functional Programming

- What is functional programming?
- What are the core principles of functional programming?
- What is referential transparency?
- What is immutability?
- What is a pure function?
- What is side-effect isolation?
- What is function composition?
- What is point-free programming?
- What is currying?
- What is partial application?
- What is a closure-based factory?
- What is a higher-order function?
- What is a reducer?
- What is a transducer?
- What is lazy evaluation?
- What is memoization?
- What is structural sharing?
- What is persistent data?
- What are algebraic data types?
- What is a discriminated union?
- What is an option or maybe type?
- What is an either/result type?
- How can functional patterns be implemented in plain JavaScript?
- What are the trade-offs of functional programming?
- How can functional code remain readable?
- How can functional code be debugged?
- When is functional programming inappropriate?

### Object-Oriented and Domain Modeling

- What is object-oriented programming?
- What are encapsulation, abstraction, inheritance, and polymorphism?
- How does JavaScript support object-oriented programming?
- What is the difference between class-based and prototype-based inheritance?
- What is composition over inheritance?
- What is dependency inversion?
- What is the single responsibility principle?
- What is the open/closed principle?
- What is the Liskov substitution principle?
- What is the interface segregation principle?
- What is the dependency inversion principle?
- How can SOLID principles be applied in JavaScript?
- What is a value object?
- What is an entity?
- What is an aggregate?
- What is a domain service?
- What is a repository abstraction?
- What is a factory?
- What is a specification pattern?
- What is a strategy pattern?
- What is a policy object?
- How should domain logic be separated from infrastructure?
- How can domain models avoid framework coupling?
- How should invariants be enforced?
- How should domain errors be modeled?
- What are anemic domain models?
- What are rich domain models?
- When should a domain model be immutable?

### Design Patterns

- What is a design pattern?
- What are creational, structural, and behavioral patterns?
- What is the factory pattern?
- What is the abstract factory pattern?
- What is the builder pattern?
- What is the singleton pattern?
- What are the risks of singletons?
- What is the module pattern?
- What is the revealing module pattern?
- What is the adapter pattern?
- What is the facade pattern?
- What is the decorator pattern?
- What is the proxy pattern?
- What is the composite pattern?
- What is the bridge pattern?
- What is the flyweight pattern?
- What is the strategy pattern?
- What is the observer pattern?
- What is the publish/subscribe pattern?
- What is the command pattern?
- What is the mediator pattern?
- What is the chain of responsibility pattern?
- What is the state pattern?
- What is the template method pattern?
- What is the iterator pattern?
- What is the visitor pattern?
- What is the dependency injection pattern?
- What is the repository pattern?
- What is the service layer pattern?
- What is the façade versus adapter distinction?
- What are the drawbacks of overusing design patterns?
- How should patterns be selected based on problem context?

### Dependency Injection and Inversion of Control

- What is dependency injection?
- What is inversion of control?
- What are constructor, property, and method injection?
- What are the benefits of dependency injection?
- What are the drawbacks of dependency injection?
- How can dependency injection be implemented without a framework?
- What is a dependency injection container?
- What is a service locator?
- Why is service locator often discouraged?
- What are dependency injection tokens?
- What is dependency inversion?
- How can dependencies be replaced in tests?
- How can dependency scopes be designed?
- What is singleton scope?
- What is transient scope?
- What is request scope?
- How can circular dependencies be detected?
- How can dependency graphs be visualized?
- How can dependency injection support plugins?
- How can dependency injection support multi-tenant applications?
- How can dependency injection be used in frontend architecture?
- How can dependency injection be used in Node.js?
- What are best practices for dependency registration?

### State Management

- What is application state?
- What is local component state?
- What is shared state?
- What is server state?
- What is URL state?
- What is derived state?
- What is normalized state?
- What is immutable state?
- What is a state machine?
- What is a finite state machine?
- What is a statechart?
- What is a reducer-based state model?
- What is event-driven state management?
- What is CQRS?
- What is event sourcing?
- What is optimistic UI?
- What is pessimistic UI?
- What is state synchronization?
- What is state hydration?
- What is state persistence?
- What is state rehydration?
- How should state be split by ownership?
- How can state updates be made predictable?
- How can state transitions be tested?
- How can stale state be avoided?
- How can race conditions in state updates be prevented?
- How should undo/redo be implemented?
- How should state be serialized?
- How should sensitive state be protected?
- What are the trade-offs of global state stores?

### Event Bus and Pub/Sub

- What is an event bus?
- What is publish/subscribe?
- What is the difference between pub/sub and observer?
- How can a typed event bus be implemented?
- How can event handlers be registered?
- How can event handlers be removed?
- How can one-time listeners be implemented?
- How can event priorities be supported?
- How can event ordering be maintained?
- How can event errors be isolated?
- How can event delivery be retried?
- How can event duplication be handled?
- What are the risks of global event buses?
- How can event buses create hidden coupling?
- How can event schemas be versioned?
- How can event buses be tested?
- When should direct function calls be preferred over events?

### Plugin and Extensibility Architecture

- What is a plugin architecture?
- What is an extension point?
- What is a hook-based architecture?
- What is a middleware pipeline?
- What is a lifecycle hook?
- What is inversion of control in plugin systems?
- How can plugins be registered dynamically?
- How can plugin dependencies be managed?
- How can plugin versions be handled?
- How can plugin isolation be achieved?
- How can untrusted plugins be sandboxed?
- How can plugin capabilities be restricted?
- How can plugins communicate with the host application?
- How can plugins be loaded lazily?
- How can plugin contracts be validated?
- How can plugins be enabled or disabled at runtime?
- How can plugin failures be isolated?
- How can plugin telemetry be collected?
- How should plugin APIs be versioned?
- How can a plugin marketplace be designed?
- What are the security risks of dynamic plugins?

### Middleware and Pipelines

- What is middleware?
- What is the onion middleware model?
- What is the difference between middleware and interceptors?
- How can middleware be composed?
- What is next-function control flow?
- What happens when middleware does not call `next()`?
- How can middleware errors be propagated?
- How can middleware short-circuit a request?
- How can middleware add context?
- How can middleware implement authentication?
- How can middleware implement authorization?
- How can middleware implement logging?
- How can middleware implement tracing?
- How can middleware implement retries?
- How can middleware implement rate limiting?
- How can middleware implement caching?
- How can middleware be ordered safely?
- How can middleware be tested?
- What are middleware performance costs?
- How can middleware avoid hidden side effects?

### Functional Reactive and Stream Patterns

- What is a stream abstraction?
- What is a data pipeline?
- What is map/filter/reduce over streams?
- What is lazy versus eager processing?
- What is backpressure?
- What is a fan-in pattern?
- What is a fan-out pattern?
- What is a merge operation?
- What is a zip operation?
- What is a switch-map pattern?
- What is a concat-map pattern?
- What is an exhaust-map pattern?
- What is a debounce pattern?
- What is a throttle pattern?
- What is buffering?
- What is windowing?
- What is event replay?
- How can streams be made fault tolerant?
- How can stream processing be cancelled?
- How can stream pipelines be tested?

### Web Components and Custom Elements

- What are Web Components?
- What are custom elements?
- What is the custom elements lifecycle?
- What is the shadow DOM?
- What is the difference between open and closed shadow roots?
- What is style encapsulation?
- What is the `:host` selector?
- What is `::slotted()`?
- What are slots?
- What is the light DOM?
- What is the composed event path?
- What is event retargeting?
- How can custom elements be made accessible?
- How can custom elements expose properties and attributes?
- What is attribute reflection?
- How can custom elements dispatch custom events?
- How can custom elements be integrated with frameworks?
- What are custom element upgrade timing issues?
- What are form-associated custom elements?
- How can Web Components be versioned?
- What are Web Components performance considerations?

---

## 4. Security & Reliability

### JavaScript Security Fundamentals

- What are the major security risks in JavaScript applications?
- What is the same-origin policy?
- What is origin?
- What is site versus origin?
- What is cross-origin isolation?
- What is the principle of least privilege?
- What is defense in depth?
- What is secure-by-default design?
- What is threat modeling?
- What is attack surface?
- What is trust boundary?
- What is input validation?
- What is output encoding?
- What is data sanitization?
- What is secure error handling?
- What is security logging?
- What is a security incident?
- How should client-side security limitations be communicated?
- Why must authorization always be enforced server-side?
- What sensitive information should never be placed in frontend code?

### Cross-Site Scripting

- What is cross-site scripting?
- What are reflected, stored, and DOM-based XSS?
- How does reflected XSS work?
- How does stored XSS work?
- How does DOM-based XSS work?
- What is an injection sink?
- Which DOM APIs can create XSS risks?
- Why is `innerHTML` dangerous?
- What are the risks of `outerHTML`, `insertAdjacentHTML`, and `document.write`?
- Why is `eval` dangerous?
- Why are `new Function` and string-based timers dangerous?
- What is HTML context encoding?
- What is attribute context encoding?
- What is JavaScript context encoding?
- What is URL context encoding?
- What is CSS context encoding?
- What is a Content Security Policy?
- What is a nonce-based CSP?
- What is a hash-based CSP?
- What is Trusted Types?
- What is DOMPurify?
- When should sanitization be used?
- Why is escaping not the same as sanitization?
- How can XSS enter through third-party libraries?
- How can XSS enter through Markdown or rich text?
- How can XSS enter through URL parameters?
- How can XSS enter through SVG?
- How can XSS be tested automatically?
- How can XSS prevention be enforced through code review?
- What are common XSS prevention mistakes?

### Cross-Site Request Forgery and Session Security

- What is CSRF?
- How does CSRF work?
- Why are cookie-based sessions vulnerable to CSRF?
- What is a synchronizer token?
- What is a double-submit cookie?
- What is the SameSite cookie attribute?
- What are `Strict`, `Lax`, and `None` SameSite modes?
- What are Secure and HttpOnly cookie attributes?
- What is session fixation?
- What is session hijacking?
- What is session rotation?
- What is session expiration?
- What is idle timeout?
- What is absolute timeout?
- What is refresh-token rotation?
- What is token replay?
- What is bearer-token risk?
- Where should access tokens be stored?
- What are the risks of storing tokens in localStorage?
- What is a secure cookie-based authentication architecture?
- What is origin checking?
- What is referer checking?
- How should logout be implemented?
- How should sessions be revoked?
- How should authentication state be synchronized across tabs?
- How should session expiration be handled in the UI?

### Authentication and Authorization

- What is authentication?
- What is authorization?
- What is the difference between identity and permissions?
- What is role-based access control?
- What is attribute-based access control?
- What is capability-based security?
- What is least privilege?
- What is multi-factor authentication?
- What is single sign-on?
- What is OAuth 2.0?
- What is OpenID Connect?
- What is PKCE?
- What is the authorization code flow?
- What is an access token?
- What is a refresh token?
- What is token expiration?
- What is token audience?
- What is token issuer?
- What is JWT?
- What are JWT security pitfalls?
- What is token validation?
- What is token introspection?
- What is authorization code interception?
- What is clickjacking?
- What is step-up authentication?
- How should frontend route guards be designed?
- Why are frontend route guards not sufficient for security?
- How should permissions be enforced in UI components?
- How should permission failures be handled?
- How should authorization logic avoid duplication?

### Supply Chain and Dependency Security

- What is software supply-chain security?
- What is dependency confusion?
- What is typosquatting?
- What is a malicious package?
- What is a compromised maintainer account?
- What is a lockfile?
- Why should lockfiles be committed?
- What is dependency pinning?
- What are transitive dependencies?
- What is software composition analysis?
- What is an SBOM?
- What is npm audit?
- What is package provenance?
- What are signed packages?
- What is the risk of install scripts?
- What is the risk of postinstall scripts?
- How can dependencies be minimized?
- How can unused dependencies be removed?
- How should dependency updates be reviewed?
- How can vulnerable dependencies be detected in CI?
- What is Dependabot?
- What is Renovate?
- How can malicious code in dependencies be isolated?
- How should third-party scripts be loaded?
- What is Subresource Integrity?
- How can CDN dependencies be secured?
- How should package registries be controlled in enterprises?

### Prototype Pollution and Object Security

- What is prototype pollution?
- How does prototype pollution occur?
- Why are `__proto__`, `constructor`, and `prototype` dangerous?
- Which merge utilities are vulnerable to prototype pollution?
- How can query-string parsing cause prototype pollution?
- How can JSON input cause prototype pollution?
- How can prototype pollution affect authorization?
- How can prototype pollution affect application logic?
- How can null-prototype objects reduce risk?
- How can keys be validated?
- Why should untrusted keys not be assigned blindly?
- How can `Object.hasOwn()` help?
- How can prototype pollution be detected?
- How can dependencies be scanned for prototype pollution?
- What are safe object merge patterns?
- How can prototype pollution be tested?

### Supply of Untrusted Content

- What is content injection?
- What is HTML injection?
- What is CSS injection?
- What is JavaScript injection?
- What is URL injection?
- What is open redirect?
- What is URL allowlisting?
- What is URL parsing confusion?
- How can `javascript:` URLs be prevented?
- How can `data:` URLs be restricted?
- How can unsafe redirects be prevented?
- How should external links use `rel="noopener"`?
- What is reverse tabnabbing?
- How should user-generated content be rendered?
- How should Markdown be sanitized?
- How should rich text editors be secured?
- How can SVG uploads be secured?
- How can file names and MIME types be validated?
- How can content-disposition be used safely?

### Browser Security Policies

- What is Content Security Policy?
- What is Permissions Policy?
- What is Cross-Origin Resource Policy?
- What is Cross-Origin Opener Policy?
- What is Cross-Origin Embedder Policy?
- What is Cross-Origin Resource Sharing?
- What is the difference between CORS and CSRF?
- What is a preflight request?
- What are simple CORS requests?
- What are credentialed CORS requests?
- Why can wildcard origins not be used with credentials?
- What are CORS response headers?
- What is opaque response behavior?
- What is mixed content?
- What is HTTPS?
- What is HSTS?
- What is certificate validation?
- What is secure context?
- What is browser isolation?
- What is iframe sandboxing?
- What is `postMessage` security?
- How should `postMessage` origins be validated?
- What are clickjacking protections?
- What is frame-ancestors?
- What are browser storage security considerations?

### Reliability Engineering

- What is reliability?
- What is availability?
- What is resilience?
- What is fault tolerance?
- What is graceful degradation?
- What is fail-safe behavior?
- What is fail-fast behavior?
- What is a single point of failure?
- What is redundancy?
- What is retry storm behavior?
- What is a circuit breaker?
- What is a bulkhead?
- What is a timeout budget?
- What is an error budget?
- What is a service-level objective?
- What is a service-level indicator?
- What is a service-level agreement?
- What is graceful shutdown?
- What is health checking?
- What is readiness versus liveness?
- What is chaos engineering?
- What is fault injection?
- How can frontend applications degrade gracefully?
- How can stale data be used safely?
- How can offline behavior be designed?
- How can partial API failures be represented?
- How can feature flags reduce deployment risk?
- How can rollback strategies be designed?
- How can reliability be measured from the browser?

### Secure Coding Practices

- How should untrusted input be validated?
- How should output be encoded?
- How should secrets be handled?
- Why should secrets never be embedded in frontend bundles?
- How should environment variables be managed?
- What is the difference between public configuration and secrets?
- How should logs avoid sensitive data?
- How should error messages avoid internal details?
- How should dependency versions be managed?
- How should security headers be configured?
- How should authentication failures be handled?
- How should authorization failures be handled?
- How should security-sensitive code be reviewed?
- What is secure default configuration?
- What is fail-closed behavior?
- How can static analysis improve security?
- How can dynamic testing improve security?
- How can security checks be integrated into CI/CD?
- How should security vulnerabilities be triaged?
- How should security regressions be prevented?

---

## 5. Performance Engineering

### Performance Fundamentals

- What is web performance?
- What is perceived performance?
- What is objective performance?
- What is latency?
- What is throughput?
- What is responsiveness?
- What is scalability?
- What is efficiency?
- What is the difference between CPU-bound and I/O-bound work?
- What is the critical rendering path?
- What is time to first byte?
- What is first contentful paint?
- What is largest contentful paint?
- What is first input delay?
- What is interaction to next paint?
- What is cumulative layout shift?
- What is total blocking time?
- What is time to interactive?
- What is speed index?
- What is a performance budget?
- What is a performance regression?
- How should performance requirements be defined?
- How should performance be measured on real devices?
- What is the difference between lab and field data?
- What is RUM?
- What is synthetic monitoring?
- How should performance be prioritized?

### JavaScript Execution Performance

- What makes JavaScript slow?
- What is the cost of parsing JavaScript?
- What is the cost of compiling JavaScript?
- What is the cost of executing JavaScript?
- What is the cost of garbage collection?
- What are long tasks?
- How can long tasks be identified?
- How can large functions be split?
- What is code splitting?
- What is lazy loading?
- What is tree shaking?
- What is dead-code elimination?
- What is minification?
- What is compression?
- What is JIT warm-up?
- What is deoptimization?
- What are hidden classes?
- What are inline caches?
- What is monomorphic code?
- What is polymorphic code?
- What is megamorphic code?
- What are allocation hotspots?
- How can object allocations be reduced?
- How can unnecessary closures be reduced?
- How can repeated calculations be avoided?
- What is memoization?
- When can memoization hurt performance?
- What is algorithmic complexity?
- What is Big O notation?
- How can O(n²) algorithms be optimized?
- How can data structures improve performance?
- What is the performance difference between arrays, objects, maps, and sets?
- How can loops be optimized without harming readability?
- When does micro-optimization matter?
- How can performance optimizations be validated?

### Rendering and Layout Performance

- What is the browser rendering pipeline?
- What are style calculation, layout, paint, and compositing?
- What is layout thrashing?
- What causes forced synchronous layout?
- What is reflow?
- What is repaint?
- What is compositing?
- Which CSS properties trigger layout?
- Which CSS properties trigger paint?
- Which CSS properties are usually compositor-friendly?
- What is the difference between transform and top/left animation?
- What is the role of `will-change`?
- Why can excessive `will-change` hurt performance?
- What is containment?
- What are CSS containment properties?
- What is `content-visibility`?
- What is `contain-intrinsic-size`?
- How can offscreen content be optimized?
- How can DOM size affect performance?
- What is DOM virtualization?
- What is list virtualization?
- How can layout shifts be prevented?
- How can image dimensions reduce layout shifts?
- What is font loading layout shift?
- How can animations respect reduced motion?
- How can rendering performance be profiled?
- What are style recalculation costs?
- How can CSS selectors affect performance?
- How can excessive nesting affect CSS performance?
- How can large DOM trees be avoided?

### Memory Management

- What is memory allocation?
- What is garbage collection?
- What are strong references?
- What are weak references?
- What is `WeakMap`?
- What is `WeakRef`?
- What is `FinalizationRegistry`?
- Why should `WeakRef` be used cautiously?
- What is a memory leak?
- What are common causes of browser memory leaks?
- How can event listeners cause memory leaks?
- How can timers cause memory leaks?
- How can closures cause memory leaks?
- How can detached DOM nodes cause memory leaks?
- How can caches cause memory leaks?
- How can subscriptions cause memory leaks?
- How can promises retain memory?
- How can memory leaks be detected?
- What are heap snapshots?
- What is allocation instrumentation?
- What is retained size?
- What is shallow size?
- What is dominator tree analysis?
- How can memory growth be monitored?
- What is a memory budget?
- How can large objects be released?
- How can cache eviction be designed?
- What are LRU and LFU caches?
- How should memory behavior be tested?

### Network Performance

- What is network latency?
- What is bandwidth?
- What is connection establishment cost?
- What is DNS lookup?
- What is TCP handshake?
- What is TLS handshake?
- What is HTTP/1.1?
- What is HTTP/2?
- What is HTTP/3?
- What is connection reuse?
- What is multiplexing?
- What is head-of-line blocking?
- What is compression?
- What is Brotli?
- What is gzip?
- What is content negotiation?
- What is cache-control?
- What is ETag?
- What is Last-Modified?
- What is stale-while-revalidate?
- What is stale-if-error?
- What is CDN caching?
- What is browser caching?
- What is service worker caching?
- What is preconnect?
- What is dns-prefetch?
- What is preload?
- What is prefetch?
- What is modulepreload?
- What is priority hints?
- What is request prioritization?
- How can waterfall requests be reduced?
- How can API payloads be reduced?
- How can duplicate requests be avoided?
- How can request batching be implemented?
- How can network retries harm performance?
- How can slow networks be handled gracefully?

### Loading and Bundling

- What is bundling?
- What is code splitting?
- What is route-level splitting?
- What is component-level splitting?
- What is dynamic import?
- What is lazy loading?
- What is eager loading?
- What is tree shaking?
- What is scope hoisting?
- What is minification?
- What is mangling?
- What is source map generation?
- What is bundle analysis?
- What is a dependency graph?
- What is a chunk?
- What is a vendor chunk?
- What is a runtime chunk?
- What is module federation?
- What are the trade-offs of microfrontends?
- What is bundle duplication?
- How can duplicate dependencies be detected?
- What is side-effect analysis?
- How can CSS be split?
- What is critical CSS?
- What is unused CSS?
- How can third-party scripts be delayed?
- How can analytics scripts be loaded efficiently?
- What is import-on-interaction?
- What is import-on-visibility?
- How should bundle budgets be enforced?

### Caching

- What is caching?
- What are browser, memory, HTTP, CDN, and service worker caches?
- What is cache invalidation?
- What is cache freshness?
- What is cache revalidation?
- What is cache busting?
- What is content hashing?
- What is immutable caching?
- What is stale-while-revalidate?
- What is cache-first?
- What is network-first?
- What is stale-while-revalidate strategy?
- What is network-only?
- What is cache-only?
- What is a cache stampede?
- What is request coalescing?
- What is cache warming?
- What is cache eviction?
- What is negative caching?
- What is cache poisoning?
- How can sensitive data be prevented from being cached?
- How should API responses be cached?
- How should user-specific data be cached?
- How should cache keys be designed?
- How can cache consistency be maintained?
- How should offline caches be versioned?
- How should service worker caches be invalidated?

### Performance Measurement and Profiling

- What is profiling?
- What is benchmarking?
- What is a microbenchmark?
- What is a macrobenchmark?
- What is a representative workload?
- What is the Performance API?
- What is `performance.now()`?
- What is the User Timing API?
- What are performance marks and measures?
- What is the Navigation Timing API?
- What is the Resource Timing API?
- What is the Paint Timing API?
- What is the Long Tasks API?
- What is the Event Timing API?
- What is the Layout Instability API?
- What is `PerformanceObserver`?
- How can custom performance metrics be collected?
- How can performance data be correlated with user actions?
- What is Chrome DevTools Performance panel?
- What is the Memory panel?
- What is the Network panel?
- What is Lighthouse?
- What is PageSpeed Insights?
- What is WebPageTest?
- What is Core Web Vitals?
- How can performance budgets be enforced in CI?
- How can performance regressions be detected automatically?
- What is statistical significance in benchmarking?
- Why should benchmarks include warm-up and repeated runs?
- How can noisy benchmark results be handled?

### Performance Architecture

- How should performance be considered during system design?
- What is performance-by-design?
- What is progressive enhancement?
- What is progressive hydration?
- What is partial hydration?
- What is resumability?
- What is server-side rendering?
- What is static site generation?
- What is incremental static regeneration?
- What is streaming rendering?
- What is edge rendering?
- What is island architecture?
- What is client-side rendering?
- What are the trade-offs between rendering strategies?
- How can hydration costs be reduced?
- How can JavaScript execution be minimized?
- How can critical user journeys be optimized?
- How should performance budgets differ by route?
- How can third-party code be isolated?
- How can performance be preserved in microfrontends?
- How can performance be maintained across low-end devices?
- How should performance ownership be distributed across teams?

---

## 6. Browser & Platform APIs

### DOM Fundamentals

- What is the DOM?
- How is the DOM different from HTML?
- How is the DOM different from the render tree?
- What is a document?
- What is an element node?
- What is a text node?
- What is a comment node?
- What is a document fragment?
- What is the difference between `Node`, `Element`, and `HTMLElement`?
- What is the difference between `querySelector` and `getElementById`?
- What is the difference between `querySelectorAll` and `getElementsByClassName`?
- What is a live collection?
- What is a static collection?
- What is `NodeList`?
- What is `HTMLCollection`?
- How can DOM nodes be created?
- How can DOM nodes be inserted?
- How can DOM nodes be removed?
- What is `append` versus `appendChild`?
- What is `prepend`?
- What is `before` and `after`?
- What is `replaceWith`?
- What is `cloneNode`?
- What is `DocumentFragment`?
- What is `textContent` versus `innerText`?
- What is `innerHTML`?
- What are DOM mutation risks?
- What is event delegation?
- What is DOM traversal?
- What is the difference between attributes and properties?
- What is attribute reflection?
- What is `dataset`?
- What is `classList`?
- What is `style`?
- How can DOM operations be batched?
- How can DOM updates avoid layout thrashing?

### Events

- What is an event?
- What is event dispatch?
- What is event bubbling?
- What is event capturing?
- What is event propagation?
- What is event delegation?
- What is the event target?
- What is the current target?
- What is `event.composedPath()`?
- What is `stopPropagation()`?
- What is `stopImmediatePropagation()`?
- What is `preventDefault()`?
- What is a passive event listener?
- What is a once event listener?
- What is an abortable event listener?
- What is the difference between `onclick` and `addEventListener`?
- What is the difference between mouse, pointer, and touch events?
- What is pointer capture?
- What are keyboard events?
- What is focus management?
- What are input, change, and beforeinput events?
- What are composition events?
- What are drag-and-drop events?
- What are clipboard events?
- What are custom events?
- How can custom event payloads be designed?
- How can event listener cleanup be guaranteed?
- How can event handlers avoid memory leaks?
- How can event ordering be tested?
- What are event security concerns?

### Forms and Validation

- What are form controls?
- What is form submission?
- What is the difference between `input` and `change`?
- What is constraint validation?
- What are native validation attributes?
- What is `checkValidity()`?
- What is `reportValidity()`?
- What is `setCustomValidity()`?
- What is `FormData`?
- How can files be submitted with `FormData`?
- What is the difference between `application/x-www-form-urlencoded`, `multipart/form-data`, and JSON?
- How can forms be progressively enhanced?
- How should client-side validation differ from server-side validation?
- How can validation errors be made accessible?
- How can asynchronous validation be implemented?
- How can duplicate submissions be prevented?
- How should form state be preserved?
- How should sensitive form data be handled?
- How can form submission be cancelled?
- What is the `requestSubmit()` method?
- What is the difference between `submit()` and `requestSubmit()`?
- How can custom form controls participate in validation?
- What are form-associated custom elements?
- How should file uploads be validated?
- How should autocomplete and autofill be handled?

### Browser Storage

- What is localStorage?
- What is sessionStorage?
- What are the differences between localStorage and sessionStorage?
- What is IndexedDB?
- What are cookies?
- What are Cache Storage APIs?
- What are storage quotas?
- What is storage partitioning?
- What is the Storage API?
- What is `navigator.storage.persist()`?
- What is the difference between persistent and best-effort storage?
- What are storage eviction rules?
- What are the security risks of localStorage?
- What are the security risks of cookies?
- What is HttpOnly?
- What is Secure?
- What is SameSite?
- How should authentication data be stored?
- How should sensitive data be encrypted at rest in browser storage?
- How should storage migrations be handled?
- How can IndexedDB transactions be designed?
- What are IndexedDB object stores and indexes?
- What are IndexedDB version upgrades?
- How can IndexedDB errors be handled?
- How can storage be tested?
- How can cross-tab storage synchronization be implemented?

### Fetch and Networking APIs

- What is the Fetch API?
- What is a `Request`?
- What is a `Response`?
- What is a `Headers` object?
- What is the difference between fetch rejection and HTTP error status?
- Why does `fetch()` not reject for HTTP 4xx or 5xx responses?
- How should HTTP errors be handled?
- What is response streaming?
- What is `response.body`?
- What is `response.json()`?
- What is `response.text()`?
- What is `response.blob()`?
- What is `response.arrayBuffer()`?
- What is `response.formData()`?
- What is `Response.clone()`?
- What is request cloning?
- What is an abort signal?
- What is CORS mode?
- What is credentials mode?
- What is cache mode?
- What is redirect mode?
- What is referrer policy?
- What is integrity metadata?
- What is keepalive?
- What is priority?
- How can fetch requests be retried safely?
- How can fetch requests be timed out?
- How can fetch requests be deduplicated?
- How can fetch response caching be designed?
- How can fetch interceptors be implemented?
- How can network failures be distinguished from server failures?
- How can API clients be made observable?
- How can request tracing be implemented?

### Web Workers and Parallelism

- What is a Web Worker?
- What is the difference between dedicated and shared workers?
- What is a service worker?
- How does a worker communicate with the main thread?
- What is `postMessage()`?
- What is the structured clone algorithm?
- What are transferable objects?
- What is an `ArrayBuffer` transfer?
- What is a `MessageChannel`?
- What is `MessagePort`?
- What is `SharedArrayBuffer`?
- What are `Atomics`?
- What is cross-origin isolation?
- What workloads belong in workers?
- What workloads should not be moved to workers?
- How can workers be pooled?
- How can worker errors be handled?
- How can workers be terminated?
- How can worker startup cost be reduced?
- How can worker messages be versioned?
- How can worker communication be typed?
- How can worker memory be controlled?
- How can worker tasks be cancelled?
- How can worker-based systems be tested?

### Service Workers and PWA

- What is a service worker?
- What is the service worker lifecycle?
- What are install, activate, and fetch events?
- What is service worker scope?
- What is service worker registration?
- What is service worker update behavior?
- What is `skipWaiting()`?
- What is `clientsClaim()`?
- What is the difference between waiting and active workers?
- What is Cache Storage?
- What is a cache-first strategy?
- What is network-first?
- What is stale-while-revalidate?
- What is offline fallback?
- What is background sync?
- What is periodic background sync?
- What are push notifications?
- What is the Push API?
- What is the Notifications API?
- What is a web app manifest?
- What makes a web app installable?
- What is an app shell?
- What are service worker security constraints?
- How can service worker updates be tested?
- How can stale assets be avoided?
- How can service worker failures be recovered?
- What are common service worker caching bugs?
- How should service workers be monitored in production?

### Web Components and Shadow DOM

- What is the custom elements registry?
- What is `customElements.define()`?
- What is `customElements.whenDefined()`?
- What is the custom element constructor?
- What are connected and disconnected callbacks?
- What are adopted and attribute-changed callbacks?
- What is `observedAttributes`?
- What is shadow DOM encapsulation?
- What is the difference between open and closed shadow roots?
- What is slot distribution?
- What is slot fallback content?
- What is event retargeting?
- What is composed event behavior?
- How do styles cross shadow boundaries?
- What are CSS custom properties in shadow DOM?
- What is `::part`?
- What is `::theme`?
- How can accessibility be implemented in custom elements?
- How can custom elements participate in forms?
- How can custom elements be tested?
- How can custom elements be integrated with Angular, React, or Vue?

### Observers and Visibility APIs

- What is `MutationObserver`?
- What is `ResizeObserver`?
- What is `IntersectionObserver`?
- What is `PerformanceObserver`?
- What is `ReportingObserver`?
- How does `MutationObserver` scheduling work?
- How can mutation observer loops be avoided?
- How can resize observer loops be avoided?
- How can lazy loading use IntersectionObserver?
- How can infinite scrolling use IntersectionObserver?
- How can visibility-based analytics be implemented?
- How can resize observation avoid layout thrashing?
- How can performance entries be observed?
- How can browser deprecation reports be collected?
- How should observers be disconnected?
- What are observer memory considerations?

### Graphics and Media

- What is Canvas?
- What is SVG?
- What is the difference between Canvas and SVG?
- What is WebGL?
- What is WebGPU?
- What is OffscreenCanvas?
- What is the Canvas 2D context?
- How can canvas rendering be optimized?
- How can high-DPI canvas rendering be handled?
- What is image decoding?
- What is `createImageBitmap()`?
- What is the ImageBitmap API?
- What are audio and video elements?
- What is Media Source Extensions?
- What is Encrypted Media Extensions?
- What is Web Audio API?
- What is WebCodecs?
- What is the Media Capture and Streams API?
- What is screen capture?
- What are permission requirements for media APIs?
- How should media resources be released?
- How can media playback errors be handled?
- How can graphics work be moved off the main thread?

### Clipboard, Notifications, and Permissions

- What is the Clipboard API?
- What is the difference between text and rich clipboard access?
- What permissions are required for clipboard access?
- What is the Notifications API?
- What is the Push API?
- What is the Permissions API?
- How can permissions be queried?
- How should denied permissions be handled?
- How can permission prompts be timed appropriately?
- What are privacy risks of permission-heavy applications?
- How should permission state be synchronized?
- How can browser capability detection be implemented?
- What is progressive enhancement for browser APIs?

### Accessibility APIs and UX

- What is accessibility?
- What is the accessibility tree?
- What is ARIA?
- What is the difference between semantic HTML and ARIA?
- What is the first rule of ARIA?
- What are roles, states, and properties?
- What is keyboard accessibility?
- What is focus management?
- What is focus trapping?
- What is a roving tabindex?
- What is `aria-live`?
- What is `aria-describedby`?
- What is `aria-labelledby`?
- What is `aria-hidden`?
- What is inert?
- What is reduced motion?
- What is high contrast support?
- How should custom controls be made accessible?
- How should modal dialogs be implemented accessibly?
- How should menus, tabs, accordions, and comboboxes be implemented?
- How should accessibility be tested automatically and manually?
- What are common accessibility regressions?

### URL, History, and Navigation APIs

- What is the URL API?
- What is `URLSearchParams`?
- How should query parameters be encoded?
- What is URL normalization?
- What is the History API?
- What are `pushState` and `replaceState`?
- What is the `popstate` event?
- How can client-side routing be implemented?
- What is the Navigation API?
- What is the difference between navigation and history manipulation?
- How can route transitions be cancelled?
- How should scroll restoration be handled?
- How should deep links be supported?
- How should URL state be validated?
- How can open redirects be prevented?
- How should navigation errors be handled?

### Timers, Idle Work, and Scheduling

- What is `setTimeout`?
- What is `setInterval`?
- What is `clearTimeout`?
- What is `clearInterval`?
- What is `requestAnimationFrame`?
- What is `requestIdleCallback`?
- What is `queueMicrotask`?
- What is the Scheduler API?
- How can idle work be scheduled?
- How can animation loops be stopped?
- How can timers be cleaned up?
- What is timer drift?
- How can recurring tasks avoid drift?
- How can background work avoid affecting input responsiveness?
- How can scheduled work be cancelled?
- How should timer-driven code be tested?

---

## 7. Tooling & Ecosystem

### Package Management

- What is npm?
- What is a package manager?
- What is the difference between npm, Yarn, pnpm, and Bun?
- What is `package.json`?
- What is `package-lock.json`?
- What is a lockfile?
- What is semantic versioning?
- What are major, minor, and patch versions?
- What are caret and tilde ranges?
- What are peer dependencies?
- What are optional dependencies?
- What are bundled dependencies?
- What are development dependencies?
- What is the difference between `dependencies` and `devDependencies`?
- What are npm scripts?
- What are lifecycle scripts?
- What is `npx`?
- What is npm workspaces?
- What is a monorepo?
- What is dependency hoisting?
- What is package resolution?
- What is package exports?
- What is package imports?
- What is the `type` field?
- What is the `main` field?
- What is the `module` field?
- What is the `browser` field?
- What is the `types` field?
- What is the `files` field?
- What is the `engines` field?
- What is the `sideEffects` field?
- What is package publishing?
- What is package provenance?
- How should package versions be managed in enterprises?
- How should dependency updates be automated?
- How should lockfile conflicts be resolved?

### Build Tools and Bundlers

- What is a build tool?
- What is a bundler?
- What is the difference between a bundler and a compiler?
- What is Webpack?
- What is Vite?
- What is Rollup?
- What is esbuild?
- What is SWC?
- What is Turbopack?
- What is Parcel?
- What is a module graph?
- What is bundling?
- What is tree shaking?
- What is code splitting?
- What are chunks?
- What are entry points?
- What are loaders?
- What are plugins?
- What are transforms?
- What is asset handling?
- What is CSS extraction?
- What is hot module replacement?
- What is fast refresh?
- What is development versus production build behavior?
- What is source map generation?
- What is incremental compilation?
- What is caching in build systems?
- What is persistent build caching?
- What is build reproducibility?
- What is deterministic output?
- How can build performance be improved?
- How can bundle size be analyzed?
- How can build configuration be maintained?

### Transpilation and Compilation

- What is transpilation?
- Why is transpilation needed?
- What is Babel?
- What is SWC?
- What is TypeScript compilation?
- What is the difference between TypeScript transpilation and type checking?
- What is a Babel preset?
- What is a Babel plugin?
- What is a target environment?
- What is browserslist?
- What is polyfilling?
- What is transpiling syntax versus polyfilling APIs?
- What is `core-js`?
- What is differential serving?
- What is legacy browser support?
- What are source maps?
- What are inline, external, and hidden source maps?
- What are decorator transforms?
- What are class field transforms?
- What are module transforms?
- What are build-time versus runtime transformations?
- How can transpilation affect bundle size?
- How can transpilation affect debugging?
- How should build targets be selected?

### TypeScript for JavaScript Architects

- What is TypeScript?
- What are the benefits and limitations of TypeScript?
- What is structural typing?
- What is nominal typing?
- What are primitive types?
- What are union types?
- What are intersection types?
- What are literal types?
- What are tuples?
- What are enums?
- What are interfaces?
- What are type aliases?
- What are generics?
- What are generic constraints?
- What are conditional types?
- What are mapped types?
- What are template literal types?
- What are utility types?
- What is `unknown`?
- What is `any`?
- What is `never`?
- What is `void`?
- What is type narrowing?
- What are type guards?
- What are discriminated unions?
- What is exhaustive checking?
- What is declaration merging?
- What are ambient declarations?
- What are module declarations?
- What is declaration emit?
- What is `tsconfig.json`?
- What is strict mode in TypeScript?
- What are `strictNullChecks`?
- What is `noImplicitAny`?
- What is `noUncheckedIndexedAccess`?
- What is `exactOptionalPropertyTypes`?
- What is `isolatedModules`?
- What is `verbatimModuleSyntax`?
- What is the difference between `target` and `module`?
- What is the difference between `moduleResolution` strategies?
- How should TypeScript be used at API boundaries?
- How can runtime validation complement static typing?
- What are the risks of type assertions?
- What are the risks of non-null assertions?
- How should types be organized in large applications?
- How should generated types be managed?
- How can TypeScript build performance be improved?

### Linting and Formatting

- What is linting?
- What is ESLint?
- What is a lint rule?
- What is a plugin?
- What is a shareable configuration?
- What is flat config?
- What is the difference between ESLint and TypeScript compiler checks?
- What is Prettier?
- Why should formatting be automated?
- What is the difference between linting and formatting?
- How can ESLint and Prettier work together?
- What is lint-staged?
- What are pre-commit hooks?
- What is Husky?
- How should lint rules be selected?
- Which lint rules improve correctness?
- Which lint rules improve security?
- Which lint rules improve maintainability?
- How should lint exceptions be documented?
- How can linting be integrated into CI?
- How can linting performance be improved?
- How should custom lint rules be developed?

### Testing

- What is unit testing?
- What is integration testing?
- What is end-to-end testing?
- What is component testing?
- What is contract testing?
- What is snapshot testing?
- What is mutation testing?
- What is property-based testing?
- What is fuzz testing?
- What is test-driven development?
- What is behavior-driven development?
- What is a test double?
- What is a stub?
- What is a mock?
- What is a spy?
- What is a fake?
- What is dependency injection for testing?
- What is test isolation?
- What is test determinism?
- What is flaky testing?
- What causes flaky tests?
- How can asynchronous tests be written reliably?
- How can timers be mocked?
- How can network requests be mocked?
- What is MSW?
- What is Jest?
- What is Vitest?
- What is Mocha?
- What is Jasmine?
- What is Playwright?
- What is Cypress?
- What is Webdriver-based testing?
- How should browser APIs be mocked?
- How should service workers be tested?
- How should Web Workers be tested?
- How should accessibility be tested?
- How should performance be tested?
- How should security tests be automated?
- What is code coverage?
- What are the limitations of code coverage?
- What is branch coverage?
- What is mutation score?
- How should test suites be organized?
- How should test execution be parallelized?
- How should test failures be diagnosed?

### Debugging and Developer Experience

- What is debugging?
- How does a debugger pause execution?
- What are breakpoints?
- What are conditional breakpoints?
- What are logpoints?
- What are watch expressions?
- What is stepping over, into, and out?
- What is a call stack?
- What are scope and closure inspection?
- What are source maps?
- How can minified production errors be debugged?
- What is remote debugging?
- How can browser memory leaks be diagnosed?
- How can network failures be diagnosed?
- How can layout issues be diagnosed?
- How can event listener issues be diagnosed?
- How can race conditions be diagnosed?
- How can async stack traces be interpreted?
- What is structured logging?
- What is log correlation?
- What is diagnostic context?
- How can debug logging be disabled in production?
- How can developer tooling improve productivity?
- How should debugging information avoid leaking secrets?

### CI/CD and Release Engineering

- What is continuous integration?
- What is continuous delivery?
- What is continuous deployment?
- What is a build pipeline?
- What is a deployment pipeline?
- What is a release artifact?
- What is artifact immutability?
- What is a reproducible build?
- What is semantic release?
- What is conventional commits?
- What is changelog automation?
- What is versioning strategy?
- What is feature flagging?
- What is canary deployment?
- What is blue-green deployment?
- What is rolling deployment?
- What is a rollback?
- What is a hotfix?
- What are deployment gates?
- How should security scanning be integrated?
- How should dependency scanning be integrated?
- How should performance budgets be integrated?
- How should smoke tests be integrated?
- How should end-to-end tests be integrated?
- How should artifacts be signed?
- How should secrets be managed in CI?
- How should environment-specific configuration be managed?
- How should release observability be implemented?

### Monorepos and Architecture Tooling

- What is a monorepo?
- What are the benefits of monorepos?
- What are the drawbacks of monorepos?
- What is a workspace?
- What is package boundary enforcement?
- What is Nx?
- What is Turborepo?
- What is Lerna?
- What is pnpm workspace?
- What is dependency graph analysis?
- What is affected-project detection?
- What is remote build caching?
- What is task orchestration?
- How should shared libraries be designed?
- How can circular package dependencies be prevented?
- How should package ownership be managed?
- How should versioning work in a monorepo?
- How can monorepo builds be accelerated?
- How can architectural constraints be enforced automatically?

### Observability and Monitoring

- What is observability?
- What are logs, metrics, and traces?
- What is distributed tracing?
- What is a trace ID?
- What is a span ID?
- What is correlation ID?
- What is frontend error monitoring?
- What is source map upload?
- What is session replay?
- What are privacy risks of session replay?
- What is real user monitoring?
- What is synthetic monitoring?
- What are custom business metrics?
- How can frontend errors be grouped?
- How can error noise be reduced?
- How can performance metrics be correlated with releases?
- How can browser errors be sent securely?
- What should never be logged?
- How should monitoring affect application performance?
- How should alert thresholds be selected?
- How can observability support incident response?

---

## 8. Beyond the Browser (Node.js & Server-Side JavaScript)

### Node.js Fundamentals

- What is Node.js?
- How is Node.js different from browser JavaScript?
- What is the V8 engine's role in Node.js?
- What is libuv?
- What is the Node.js event loop?
- What are Node.js runtime APIs?
- What is the difference between Node.js and a browser host environment?
- What is the global object in Node.js?
- What is `globalThis` in Node.js?
- What is the `process` object?
- What is `process.argv`?
- What is `process.env`?
- What is `process.cwd()`?
- What is `__dirname`?
- What is `__filename`?
- Why are `__dirname` and `__filename` unavailable in native ES modules?
- How can file URLs be converted to paths?
- What is `process.nextTick()`?
- What is `setImmediate()`?
- What is `process.hrtime.bigint()`?
- What is `process.memoryUsage()`?
- What is `process.version`?
- What are Node.js runtime flags?
- How can Node.js applications be configured?
- How should environment variables be validated?
- How should Node.js applications handle startup failures?

### Node.js Modules

- What is CommonJS?
- What are ES modules in Node.js?
- What is the difference between `require` and `import`?
- What is the module cache?
- What is `require.resolve()`?
- What is the Node.js module resolution algorithm?
- What is the `package.json` `type` field?
- What is the `.cjs` extension?
- What is the `.mjs` extension?
- What is the `exports` field?
- What is the `imports` field?
- What are conditional exports?
- What is dual-package support?
- What are CommonJS/ESM interoperability issues?
- What are circular dependencies in Node.js?
- What is top-level `await` in Node.js?
- What are dynamic imports in Node.js?
- What are built-in `node:` imports?
- How should internal packages be organized?
- How should package boundaries be designed?
- How should module loading be tested?

### File System

- What is the Node.js `fs` module?
- What is the difference between synchronous and asynchronous file APIs?
- When should synchronous file APIs be avoided?
- What is `fs/promises`?
- How can files be read efficiently?
- How can files be written safely?
- What is atomic file replacement?
- What are file descriptors?
- What are file permissions?
- What is the difference between `stat`, `lstat`, and `fstat`?
- How can directories be created recursively?
- How can files be copied and moved?
- How can files be watched?
- What are the limitations of `fs.watch`?
- What is recursive file watching?
- How can file paths be normalized?
- What is path traversal?
- How can path traversal be prevented?
- How should uploaded files be stored?
- How can temporary files be managed?
- How can file operations be cancelled?
- How should file-system errors be handled?
- How can file operations be tested?
- How can large files be processed without loading them into memory?

### Streams and Backpressure

- What are Node.js streams?
- What is a readable stream?
- What is a writable stream?
- What is a duplex stream?
- What is a transform stream?
- What is object mode?
- What is stream backpressure?
- What is `highWaterMark`?
- What is the `data` event?
- What is the `readable` event?
- What is the `end` event?
- What is the `finish` event?
- What is the `close` event?
- What is the `error` event?
- What is `stream.pipeline()`?
- What is `stream.finished()`?
- How can streams be composed?
- How can streams be cancelled?
- How can stream errors be handled?
- How can streams be converted to async iterables?
- How can streams process large files?
- How can streams handle slow consumers?
- What are stream memory risks?
- What are stream performance tuning techniques?
- How can streams be tested?

### HTTP and Web Servers

- What is the Node.js HTTP module?
- How can an HTTP server be created?
- What are request and response objects?
- What is HTTP keep-alive?
- What is connection pooling?
- What is request parsing?
- What is response streaming?
- What are HTTP headers?
- What is content negotiation?
- What is compression?
- What is chunked transfer encoding?
- What is HTTP timeout configuration?
- What is request timeout?
- What is headers timeout?
- What is keep-alive timeout?
- What is a reverse proxy?
- What is TLS termination?
- How can HTTPS be configured?
- What is HTTP/2 in Node.js?
- What is HTTP/3 support?
- How can graceful shutdown be implemented?
- How can connection draining be implemented?
- How can request cancellation be propagated?
- How can HTTP errors be handled?
- How can request IDs be generated?
- How can access logging be implemented?
- How can rate limiting be implemented?
- How can request body size be limited?
- How can slowloris attacks be mitigated?
- How can server performance be measured?

### Express, Fastify, and Framework Architecture

- What is Express?
- What is Fastify?
- What is NestJS?
- What are the differences between Express, Fastify, and NestJS?
- What is middleware?
- What is a route handler?
- What is a controller?
- What is a service?
- What is dependency injection in backend frameworks?
- What is request lifecycle?
- What is middleware ordering?
- What are hooks?
- What are interceptors?
- What are guards?
- What are pipes?
- What are filters?
- How should validation be implemented?
- How should serialization be implemented?
- How should error handling be centralized?
- How should authentication be implemented?
- How should authorization be implemented?
- How should request context be propagated?
- How should API versioning be implemented?
- How should OpenAPI documentation be generated?
- How should framework adapters be selected?
- How can framework overhead be measured?
- How should framework-specific code be isolated?

### REST APIs

- What is REST?
- What are REST constraints?
- What is a resource?
- What is a representation?
- What are HTTP methods?
- What is idempotency?
- What is safety in HTTP methods?
- What is the difference between PUT and PATCH?
- What is the difference between POST and PUT?
- What are HTTP status code classes?
- What is content negotiation?
- What is pagination?
- What is cursor pagination?
- What is offset pagination?
- What is filtering?
- What is sorting?
- What is searching?
- What is field selection?
- What is API versioning?
- What is HATEOAS?
- What is an idempotency key?
- What is optimistic concurrency control?
- What is ETag-based concurrency?
- How should validation errors be represented?
- How should API errors be standardized?
- How should rate-limit responses be represented?
- How should REST APIs be secured?
- How should REST APIs be documented?
- How should REST APIs be tested?
- How should backward compatibility be maintained?

### GraphQL and RPC

- What is GraphQL?
- What are queries, mutations, and subscriptions?
- What is a GraphQL schema?
- What are resolvers?
- What is the N+1 problem?
- What is DataLoader?
- What is query complexity analysis?
- What is query depth limiting?
- What is persisted queries?
- What is GraphQL introspection?
- What are GraphQL security risks?
- What is the difference between REST and GraphQL?
- What is RPC?
- What is gRPC?
- What is JSON-RPC?
- What is tRPC?
- What are schema-first and code-first approaches?
- How should APIs be versioned?
- How should API contracts be tested?
- How should API observability be implemented?

### Databases and Data Access

- What is a database connection pool?
- What is connection pooling?
- What is a transaction?
- What is isolation level?
- What is optimistic locking?
- What is pessimistic locking?
- What is an ORM?
- What is a query builder?
- What is the repository pattern?
- What is the unit-of-work pattern?
- What is the N+1 query problem?
- What is eager loading?
- What is lazy loading?
- What is pagination at the database layer?
- What is SQL injection?
- How can parameterized queries prevent SQL injection?
- What is NoSQL?
- What is document storage?
- What is key-value storage?
- What is eventual consistency?
- What is read-after-write consistency?
- What is caching at the data-access layer?
- What is cache invalidation?
- How should database errors be handled?
- How should transactions interact with retries?
- How should database connections be closed during shutdown?
- How can database performance be measured?

### Authentication and Security in Node.js

- How should passwords be hashed?
- What is bcrypt?
- What is scrypt?
- What is Argon2?
- What is password salting?
- What is password stretching?
- How should password reset flows be designed?
- How should session cookies be configured?
- How should JWTs be validated?
- What is refresh-token rotation?
- What is CSRF protection?
- What is CORS configuration?
- What is helmet?
- What is security headers configuration?
- How can request body parsing be secured?
- How can prototype pollution be prevented?
- How can path traversal be prevented?
- How can SSRF be prevented?
- What is SSRF?
- How can command injection be prevented?
- How can SQL injection be prevented?
- How can NoSQL injection be prevented?
- How can template injection be prevented?
- How can regular-expression denial of service be prevented?
- How should secrets be loaded?
- How should secret rotation be handled?
- How should audit logging be implemented?
- How should security incidents be handled?

### Worker Threads, Cluster, and Child Processes

- What are Node.js worker threads?
- When should worker threads be used?
- What is the difference between worker threads and child processes?
- What is the difference between worker threads and cluster?
- How does data transfer work between workers?
- What are transferable objects?
- What is `SharedArrayBuffer` in Node.js?
- What are `Atomics`?
- How can a worker pool be implemented?
- How can worker errors be handled?
- How can workers be terminated?
- How can worker tasks be cancelled?
- What is process isolation?
- What is the cluster module?
- How can multiple CPU cores be used?
- What are the limitations of clustering?
- What is a child process?
- What is `spawn`?
- What is `exec`?
- What is `execFile`?
- What is `fork`?
- What are shell injection risks?
- How can child-process output be streamed?
- How can child processes be monitored?
- How can worker memory be limited?
- How should worker-based systems be tested?

### Queues, Jobs, and Background Processing

- What is a job queue?
- What is background processing?
- What is a worker?
- What is delayed execution?
- What is scheduled execution?
- What is retryable work?
- What is dead-letter queue behavior?
- What is at-least-once delivery?
- What is at-most-once delivery?
- What is exactly-once processing, and why is it difficult?
- What is idempotent job processing?
- What is a poison message?
- What is backoff?
- What is job prioritization?
- What is job deduplication?
- What is job leasing?
- What is visibility timeout?
- What is distributed locking?
- What is a saga?
- What is transactional outbox?
- How can jobs be monitored?
- How can failed jobs be replayed?
- How can job payloads be versioned?
- How can queue workers shut down gracefully?
- How can queue throughput be measured?

### Logging, Metrics, and Tracing

- What is structured logging?
- What is a log level?
- What is a correlation ID?
- What is a request ID?
- What is distributed tracing?
- What is OpenTelemetry?
- What is a trace?
- What is a span?
- What is baggage?
- What is context propagation?
- How can async context be preserved in Node.js?
- What is `AsyncLocalStorage`?
- How can request context be accessed safely?
- What should be logged for each request?
- What should never be logged?
- How should PII be redacted?
- How should logs be sampled?
- What are metrics?
- What are counters, gauges, histograms, and summaries?
- What is latency percentile measurement?
- What are RED metrics?
- What are USE metrics?
- How can application errors be grouped?
- How can logs be correlated with deployments?
- How can observability overhead be controlled?

### Testing Node.js Applications

- How should Node.js unit tests be structured?
- How should HTTP APIs be tested?
- What is supertest?
- What is integration testing with a real database?
- What is testcontainers?
- How should external services be mocked?
- How should filesystem access be tested?
- How should streams be tested?
- How should worker threads be tested?
- How should child processes be tested?
- How should timers be tested?
- How should event-loop behavior be tested?
- How should race conditions be tested?
- How should graceful shutdown be tested?
- How should retry logic be tested?
- How should queue consumers be tested?
- How should authentication be tested?
- How should authorization be tested?
- How should security vulnerabilities be tested?
- How should performance tests be designed?
- How should load tests be designed?
- How should contract tests be implemented?
- How should flaky backend tests be diagnosed?

### Deployment and Runtime Operations

- How should Node.js applications be containerized?
- What is a multi-stage Docker build?
- How should a Node.js container run as a non-root user?
- How should signals be handled?
- What is graceful shutdown?
- What is readiness?
- What is liveness?
- What is health checking?
- What is horizontal scaling?
- What is vertical scaling?
- What is process management?
- What is PM2?
- What is systemd?
- What is Kubernetes deployment?
- What is a rolling update?
- What is a canary release?
- How should environment configuration be injected?
- How should secrets be injected?
- How should logs be collected?
- How should metrics be exposed?
- How should crash loops be diagnosed?
- What is a core dump?
- How can heap snapshots be collected in production safely?
- How can CPU profiling be performed in production?
- How should Node.js versions be upgraded?
- How should zero-downtime deployments be implemented?
- How should rollback be performed?
- How should runtime resource limits be configured?

### Node.js Performance and Reliability

- What causes Node.js event-loop blocking?
- How can event-loop lag be measured?
- What is CPU profiling?
- What is heap profiling?
- What is flame graph analysis?
- What is clinic.js?
- What is `perf_hooks`?
- What is `monitorEventLoopDelay()`?
- How can synchronous APIs harm server throughput?
- How can JSON serialization become a bottleneck?
- How can large JSON payloads be handled?
- How can streams improve memory usage?
- How can connection pools be tuned?
- How can database queries be optimized?
- How can caching improve throughput?
- What is backpressure in HTTP servers?
- How can memory leaks be detected in Node.js?
- How can unhandled promise rejections be handled?
- How can uncaught exceptions be handled?
- When should a process crash?
- How can graceful degradation be implemented?
- How can overload protection be implemented?
- What is load shedding?
- What is rate limiting?
- What is circuit breaking?
- How can timeouts be applied consistently?
- How can retries be prevented from amplifying outages?
- How can Node.js services be made horizontally scalable?
- How should reliability targets be measured?

### Advanced Server-Side JavaScript Architecture

- How should a large Node.js application be structured?
- What is layered architecture?
- What is hexagonal architecture?
- What is clean architecture?
- What is domain-driven design?
- What is modular monolith architecture?
- What are microservices?
- What are the trade-offs between monoliths and microservices?
- What is a backend-for-frontend?
- What is an API gateway?
- What is a service mesh?
- What is event-driven architecture?
- What is CQRS?
- What is event sourcing?
- What is a transactional outbox?
- What is a saga?
- What is eventual consistency?
- What is distributed locking?
- What is idempotency across services?
- How should service boundaries be selected?
- How should shared libraries be governed?
- How should API contracts be versioned?
- How should backward compatibility be preserved?
- How should cross-cutting concerns be implemented?
- How should configuration be managed?
- How should feature flags be managed?
- How should multi-tenancy be designed?
- How should auditability be designed?
- How should disaster recovery be designed?
- How should architecture decisions be documented?
- How should technical debt be managed?
- How should architecture evolve as traffic and teams grow?

---

## Cross-Cutting Architect-Level Questions

- How would you design a large-scale JavaScript platform from scratch?
- How would you define the architecture principles for a global frontend platform?
- How would you decide between a monolith, modular monolith, and microfrontends?
- How would you decide between REST, GraphQL, and RPC?
- How would you design a frontend platform used by multiple product teams?
- How would you design a plugin system for enterprise applications?
- How would you design a reliable API client used across hundreds of applications?
- How would you design a global error-handling strategy?
- How would you design a security model for a browser-based enterprise application?
- How would you design a secure authentication and authorization architecture?
- How would you design a state-management strategy for a large application?
- How would you design a caching strategy across browser, CDN, service worker, and server?
- How would you design a performance budget for a large product?
- How would you design an observability strategy for frontend and backend JavaScript?
- How would you design a deployment pipeline for a JavaScript monorepo?
- How would you design a zero-downtime Node.js deployment?
- How would you design a resilient system that handles partial failures?
- How would you design a retry and timeout policy for distributed services?
- How would you design cancellation across nested asynchronous operations?
- How would you design a worker pool for CPU-intensive tasks?
- How would you design a high-throughput streaming pipeline?
- How would you design an offline-first web application?
- How would you design a multi-tenant JavaScript platform?
- How would you design an extensible SDK?
- How would you design a backwards-compatible public API?
- How would you migrate a CommonJS codebase to ES modules?
- How would you migrate JavaScript to TypeScript incrementally?
- How would you improve the performance of a slow production application?
- How would you investigate a memory leak reported only in production?
- How would you investigate a growing event-loop lag problem?
- How would you investigate a sudden increase in frontend errors?
- How would you investigate a bundle-size regression?
- How would you investigate a layout-shift regression?
- How would you investigate a security vulnerability in a third-party dependency?
- How would you design coding standards for a large JavaScript organization?
- How would you establish architecture governance without blocking delivery?
- How would you evaluate a new JavaScript framework or runtime?
- How would you decide whether to adopt a new language feature?
- How would you balance developer experience, performance, security, and maintainability?
- How would you document architecture decisions?
- How would you mentor senior engineers toward architect-level thinking?
- How would you review a JavaScript architecture proposal?
- How would you identify accidental complexity in a codebase?
- How would you reduce coupling between teams and modules?
- How would you define technical health metrics?
- How would you prioritize technical debt?
- How would you plan a large-scale frontend modernization?
- How would you plan a Node.js runtime upgrade across many services?
- How would you design a platform that supports internationalization and accessibility from the beginning?
- How would you ensure architecture decisions remain aligned with business goals?

---

## Practical Coding and System-Design Exercises

- Implement a custom `Promise.all`.
- Implement a custom `Promise.race`.
- Implement a custom `Promise.allSettled`.
- Implement a custom `Promise.any`.
- Implement a promise-based timeout utility.
- Implement retry with exponential backoff and jitter.
- Implement an abortable asynchronous operation.
- Implement a concurrency limiter.
- Implement a semaphore.
- Implement a mutex.
- Implement a task queue.
- Implement a priority queue.
- Implement a promise pool.
- Implement a debounced function.
- Implement a throttled function.
- Implement a cancellable debounce.
- Implement a memoization utility.
- Implement a deep-clone utility.
- Implement a deep-freeze utility.
- Implement a safe object merge utility.
- Implement a deep-equality utility.
- Implement a custom event emitter.
- Implement an event bus with typed events.
- Implement an observable abstraction.
- Implement a pub/sub system.
- Implement a middleware pipeline.
- Implement a plugin registry.
- Implement a dependency injection container.
- Implement a state machine.
- Implement an undo/redo manager.
- Implement a cache with LRU eviction.
- Implement a stale-while-revalidate cache.
- Implement request deduplication.
- Implement a single-flight request manager.
- Implement a rate limiter.
- Implement a circuit breaker.
- Implement a retry budget.
- Implement an async iterator for paginated APIs.
- Implement an async generator for polling.
- Implement a stream transformer.
- Implement a worker-thread pool.
- Implement a file-processing pipeline using streams.
- Implement a secure URL validator.
- Implement a safe HTML rendering utility.
- Implement a schema validator.
- Implement a structured error hierarchy.
- Implement a request correlation context.
- Implement a frontend performance-monitoring utility.
- Implement a route-level code-splitting strategy.
- Implement a service worker cache strategy.
- Implement an offline queue.
- Implement a resilient API client.
- Design a secure authentication flow.
- Design a scalable frontend architecture.
- Design a plugin-based enterprise platform.
- Design a multi-tenant JavaScript application.
- Design a high-performance Node.js API.
- Design a distributed job-processing system.
- Design a browser-based collaborative editor.
- Design an offline-first application.
- Design a real-time notification system.
- Design a frontend observability platform.
- Design a secure file-upload service.
- Design a resilient payment workflow.
- Design a large-scale JavaScript monorepo.

---

## Signature

**Vedprakash**  
Front-End Architect | SAP Commerce Cloud Enthusiast | Aspiring Tech Lead  
📍 Pune, India
