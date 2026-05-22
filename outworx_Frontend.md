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
==================================================================================
1. In which scenarios are `useCallback` and `useMemo` actually useful in React?

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
 ================================================================================================

TypeScript & Node.js Interview Questions Compilation
TypeScript Fundamentals
What is TypeScript?
How is TypeScript different from JavaScript?
Why do we use TypeScript?
What are the advantages of TypeScript over JavaScript?
What is strict typing in TypeScript?
What happens during TypeScript compile time?
What is type inference in TypeScript?
Difference between interface and type
What is the difference between any, unknown, and never?
What are union types and intersection types?
What is type narrowing?
What are optional properties in TypeScript?
What is readonly in TypeScript?
What is enum in TypeScript?
What is type assertion?
Difference between == and ===
TypeScript Generics Questions
What are generics in TypeScript?
Why do we use generics?
What problem do generics solve?
Why should we avoid using any?
Difference between any and generics
How do generics improve type safety?
Explain generics with a function example.
Explain identity<T>() generic function.
What is reusable code in TypeScript generics?
How does TypeScript infer generic types?
Advanced TypeScript Generics
What is keyof in TypeScript?
What is extends in generics?
What is indexed access type (T[K])?
What is Record<string, any>?
What is mapped type in TypeScript?
What are utility types in TypeScript?
Explain Pick
Explain Omit
Explain Partial
Explain Required
What is distributive conditional type?
Explain:
Keys extends keyof T ? ... : never
How to create a custom utility type in TypeScript?
How to create a RequireAtLeastOne utility type?

array of object , key is a string
// return object which has that key

function findObject<T>(arr : T[], key extends keyof T) : T | undefined {
   
    var result = arr.find(obj =>
    {
         let keys = Object.keys(obj);
         let isAvailable =  keys.find((k) => {
             if(k=== key) return true;
         })
         if(isAvailable) return obj;
    })
   
    return result;
}

console.log(findObject([{'id' : '1'},{'name' : 'XYZ'}], 'name1'));










// // RequireAtLeastOne<T, Keys> — a TypeScript utility type where at least one of the specified Keys must be present in the object.
//  type RequireAtLeastOne<T, Keys >
 
// type SearchParams = RequireAtLeastOne<{ country?: string; region?: string; crop?: string },'country' | 'region'>

// const a: SearchParams = { country: 'DE' } // valid

// const b: SearchParams = { region: 'EU', crop: 'Wheat' } // valid
// const c: SearchParams = { crop: 'Wheat' } // ERROR — country or region required
    
