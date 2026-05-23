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
