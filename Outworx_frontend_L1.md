# TypeScript & Node.js Interview Questions Compilation

## TypeScript Fundamentals

1. What is TypeScript?
2. How is TypeScript different from JavaScript?
3. Why do we use TypeScript?
4. What are the advantages of TypeScript over JavaScript?
5. What is strict typing in TypeScript?
6. What happens during TypeScript compile time?
7. What is type inference in TypeScript?
8. Difference between `interface` and `type`
9. What is the difference between `any`, `unknown`, and `never`?
10. What are union types and intersection types?
11. What is type narrowing?
12. What are optional properties in TypeScript?
13. What is `readonly` in TypeScript?
14. What is enum in TypeScript?
15. What is type assertion?
16. Difference between `==` and `===`

---

# TypeScript Generics Questions

17. What are generics in TypeScript?
18. Why do we use generics?
19. What problem do generics solve?
20. Why should we avoid using `any`?
21. Difference between `any` and generics
22. How do generics improve type safety?
23. Explain generics with a function example.
24. Explain `identity<T>()` generic function.
25. What is reusable code in TypeScript generics?
26. How does TypeScript infer generic types?

---

# Advanced TypeScript Generics

27. What is `keyof` in TypeScript?
28. What is `extends` in generics?
29. What is indexed access type (`T[K]`)?
30. What is `Record<string, any>`?
31. What is mapped type in TypeScript?
32. What are utility types in TypeScript?
33. Explain `Pick`
34. Explain `Omit`
35. Explain `Partial`
36. Explain `Required`
37. What is distributive conditional type?
38. Explain:

```ts id="nftjlwm"
Keys extends keyof T ? ... : never
```

39. How to create a custom utility type in TypeScript?
40. How to create a `RequireAtLeastOne` utility type?

---

# Practical Generics Coding Questions

## 1. Generic Identity Function

```ts id="o88a0n"
function identity<T>(value: T): T
```

Question:

* Explain how this works.
* Why is this better than `any`?

---

## 2. Generic Array Value Extractor

Create a function:

```ts id="rbz9k1"
getValue(arr, key)
```

Requirements:

* Accept array of objects
* Accept key
* Return all values for that key

Example:

```ts id="shjlwm"
getValue(users, "name")
```

Expected:

```ts id="k9v7uu"
["Kavita", "Rahul"]
```

Follow-up:

* Explain `K extends keyof T`
* Explain `T[K]`

---

## 3. Find Object By Key

Create a function:

```ts id="3n5s81"
findObjectByKey(arr, key)
```

Requirements:

* Accept array of objects
* Return object containing provided key

Example:

```ts id="wgt7e7"
findObjectByKey(data, "name")
```

---

## 4. Find Object By Key-Value Pair

Create a function:

```ts id="8jlwmr"
findByKey(arr, key, value)
```

Example:

```ts id="rdy2jp"
findByKey(users, "id", 2)
```

Expected:

* Return matching object

---

## 5. Require At Least One Utility Type

Create custom utility type:

```ts id="j1wnfe"
RequireAtLeastOne<T, Keys>
```

Requirements:

* At least one key should be mandatory

Example:

```ts id="xjlwmv"
type SearchParams = {
  country?: string;
  region?: string;
};
```

Valid:

```ts id="8g7w1f"
{ country: "India" }
{ region: "APAC" }
{ country: "India", region: "APAC" }
```

Invalid:

```ts id="vrwutq"
{}
```

---

# Node.js Interview Questions

## Event Loop & Async

41. What happens internally when you call `async/await` in Node.js?
42. Explain Event Loop phases in Node.js.
43. Difference between `process.nextTick()` and `setImmediate()`
44. What are microtasks in Node.js?
45. What is Promise resolution queue?
46. Difference between microtask queue and callback queue
47. Explain timers phase.
48. Explain check phase.
49. Where does `setTimeout()` execute?
50. Where does `setImmediate()` execute?
51. How does Node.js handle multiple requests using a single thread?
52. What is non-blocking I/O?
53. How are I/O operations handled internally in Node.js?
54. Role of libuv in Node.js

---

# Authentication & Security

55. What is JWT?
56. How does JWT authentication work?
57. Difference between session-based auth and JWT auth
58. What is token expiration (TTL)?
59. How is JWT validated on backend?
60. What is refresh token?
61. What are authentication best practices?

---

# Database Questions

62. What is sharding?
63. What is replication in databases?
64. What is sparse index?
65. What is partial index?
66. Difference between sparse index and partial index
67. What is MongoDB aggregation?
68. What is `$group` in MongoDB?
69. What is `$lookup` in MongoDB?
70. What is `$unwind` in MongoDB?

---

# System Design & Scalability

71. What is horizontal scaling?
72. What is vertical scaling?
73. Difference between horizontal and vertical scaling
74. What is rate limiting?
75. How do you prevent API abuse?
76. What is API Gateway?
77. How does API Gateway help in microservices?
78. Difference between EC2 and Lambda
79. When would you choose Lambda over EC2?
80. Explain serverless architecture

---

# JavaScript Questions

81. What is variable shadowing in JavaScript?
82. Difference between `var`, `let`, and `const`
83. What is closure?
84. What is hoisting?
85. What is event bubbling?
86. What is event capturing?
87. What is debounce and throttle?
88. Difference between shallow copy and deep copy

---

# React Questions

89. What is React reconciliation?
90. What is virtual DOM?
91. Difference between controlled and uncontrolled components
92. What are hooks in React?
93. Difference between `useMemo` and `useCallback`
94. What is Redux?
95. Why use Redux Toolkit?
96. What is prop drilling?
97. How do you optimize React performance?

---

# AWS & Cloud

98. What is S3?
99. How file upload works in S3?
100. What is CloudFront?
101. What is IAM?
102. What is Terraform?
103. What is Jenkins?
104. Explain CI/CD pipeline.

---

# Leadership & Behavioral

105. How do you manage production issues?
106. How do you mentor junior developers?
107. How do you handle stakeholder communication?
108. Explain SOLID principles.
109. Explain DRY principle.
110. How would you divide tasks in a team?
111. How would you approach development using AI tools?
112. How do you handle conflicts in a team?
113. Describe a challenging production bug you solved.

114. 1. In which scenarios are `useCallback` and `useMemo` actually useful in React?

2. Why is there no benefit in using `useCallback` or `useMemo` when dependencies change frequently?

3. What problem do `useCallback` and `useMemo` solve in React applications?

4. Why are `useCallback` and `useMemo` commonly used when passing props to child components?

5. How does React compare primitive values versus objects/functions/arrays using strict equality (`===`)?

6. What is reference equality in JavaScript?

7. Why do objects, arrays, and functions with the same content still fail strict equality comparison?

8. Why do functions get recreated on every render in React functional components?

9. How does function reference change affect child component rendering?

10. What role does `React.memo` play in preventing unnecessary re-renders?

11. What is shallow comparison in React?

12. Are React functional components pure components by default or non-pure components?

13. What is a pure component in React?

14. How can we convert a functional component into a pure component?

15. What is the difference between `React.memo` and `PureComponent`?

16. When does a child component wrapped with `React.memo` still re-render?

17. Why does passing an object prop to a memoized child component still trigger re-rendering?

18. How does `React.memo` compare object props internally?

19. How can we control re-rendering behavior in `React.memo` using a custom comparison function?

20. How can we make a child component re-render only when a specific property of an object changes?

21. What is the purpose of the second argument in `React.memo`?

22. What should the custom comparison function in `React.memo` return to skip or allow re-rendering?

23. Why can overusing `useMemo` and `useCallback` sometimes hurt performance instead of improving it?
# React / Redux Immutability & State Management Questions

1. Why should we avoid mutating state directly in React or Redux?

2. What is immutability in JavaScript?

3. What is the difference between:

   ```js
   tasks.push(newTask)
   ```

   and

   ```js
   [...tasks, newTask]
   ```

4. Why does React prefer immutable updates?

5. How does React detect state changes internally?

6. What is shallow comparison in React?

7. Why might React not re-render when using `push()` on a state array?

8. What happens internally when the reference of an object or array does not change?

9. Why do we use:

   ```js
   setTasks(prev => [...prev, newTask])
   ```

   instead of mutating the existing array?

10. How does reference equality affect rendering in React?

11. Explain:

```js
oldArray === newArray
```

12. What are mutable and immutable operations in JavaScript arrays?

13. Which array methods mutate the original array?

* push
* pop
* splice
* shift
* unshift
* sort
* reverse

14. Which array methods return a new array?

* map
* filter
* concat
* slice
* spread operator

15. How does immutability help Redux?

16. Why are Redux reducers expected to be pure functions?

17. What problems can happen if Redux state is mutated directly?

18. Why does Redux rely on immutable updates for performance optimization?

19. How does React Redux detect state updates?

20. Why can mutating state break:

* `useEffect`
* `useMemo`
* `useCallback`
* `React.memo`

21. Explain how dependency arrays work in `useEffect`.

22. Why may `useEffect` not trigger if state is mutated directly?

23. How does `React.memo` use reference comparison?

24. What is referential equality?

25. What is the role of object references in JavaScript memory management?

26. Why does creating a new object/array help React trigger re-rendering?

27. What is the spread operator doing internally?

28. What is structural sharing in immutable updates?

29. What are the benefits of immutability?

* predictable state
* debugging
* performance optimization
* time-travel debugging

30. Why is direct mutation considered an anti-pattern in React?

31. How does Redux Toolkit allow writing mutating-looking code safely?

32. What is [Immer](https://immerjs.github.io/immer/?utm_source=chatgpt.com) and how does it work?

33. Why does this work in Redux Toolkit?

```js
state.tasks.push(newTask)
```

34. Difference between manual immutable updates and Immer-based updates.

35. What is the connection between immutability and virtual DOM optimization?

36. Can React always detect deep mutations inside objects?

37. What are the performance implications of immutable state updates?

38. Explain state mutation with a real-world UI rendering example.

39. What is the difference between deep copy and shallow copy?

40. When should we avoid unnecessary object recreation in React?
## React / Frontend

1. What is the difference between local state and global state?
2. Which React hooks have you used in your project?
3. Have you created custom hooks? What reusable hooks/functions did you build?
4. What is the purpose of `useEffect` in functional components?
5. What happens if a state variable is added in the dependency array and its setter is also called inside `useEffect`?
6. What are the use cases of `useEffect`?
7. What is the difference between `useCallback` and `useMemo`?
8. What is the purpose of `React.memo`?
9. If a parent component re-renders, will the child component also re-render?
10. If a child component is wrapped with `React.memo`, will it still re-render when the parent re-renders?
11. Why are `useCallback` and `useMemo` often used together with `React.memo`?
12. How can you prevent unnecessary API calls during frequent re-rendering?
13. How would you optimize performance in React applications with heavy re-rendering?

---

## Redux / State Management

14. Since your project was using Redux and not Redux Toolkit, how were you managing state?
15. What is the difference between traditional Redux and Redux Toolkit?
16. Have you used RTK Query?
17. How does Redux help avoid repeated API calls?
18. How would you cache API responses in frontend applications?

---

## Caching / Performance

19. On what basis would you choose between Redis, Node Cache, or LRU Cache?
20. What are the advantages of Redis over in-memory caching?
21. What are the use cases of LRU cache?
22. How do you decide whether to use local cache or distributed cache?

---

## Architecture / Decision Making

23. Were you part of the team that decided to use Reddit, or was it already implemented before you joined?
24. What was the use case behind that technical decision?

---

## MongoDB / Database

25. In what format is data stored in MongoDB?
26. What is BSON in MongoDB?
27. What is the maximum document size in MongoDB?
28. What is GridFS and why is it used?
29. What is the purpose of the `_id` field in MongoDB?
30. Can we create custom `_id` values ourselves?
31. Does MongoDB ensure uniqueness of `_id` values?
32. Were you using `find()` queries or aggregation pipelines for fetching data?
33. When would you use `find()` versus aggregation pipeline?
34. Have you used `$group` in MongoDB aggregation?
35. Have you used `$lookup` in MongoDB aggregation?
36. What is `$unwind` in MongoDB aggregation pipeline?
37. What are sharding and replication in MongoDB?
38. What is the difference between sharding and replication?
39. Have you used sparse index or partial index?
40. What is a partial index in MongoDB?
41. What is the difference between sparse index and partial index?

1. Do you know about Event Loop queues/phases in Node.js? Which are those queues/phases?

2. In case of Event Loop, can you explain the Poll phase?

3. How does Node.js ensure that the single thread is not blocked while asynchronous tasks like API calls are running?

4. What are some design patterns used in day-to-day development?

5. Among callbacks, event-driven, streams, promises, and async-await, which one is most commonly used nowadays and why?

6. Explain callback hell with an example.

7. In callback hell, how are sequential/dependent operations handled?

8. What happens if an intermediate API (like getOrders) fails in callback hell?

9. What happens if we remove `async` from an async function? Does the function still behave asynchronously?

10. What actually makes a function asynchronous in JavaScript/Node.js?

11. Have you implemented anything specifically related to application security?

12. How did you make the application/API more secure?

13. Was login implemented using local authentication or OAuth 2.0/SSO?

14. How was authentication/session handling managed after login?

15. How does JWT-based authentication work?

16. How is JWT authentication different from traditional session-based authentication?

17. In JWT authentication, how does backend validate the user without checking the session database every time?

18. Why is JWT called stateless authentication?


