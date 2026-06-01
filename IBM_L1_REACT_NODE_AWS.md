React Questions
---------------
React Hooks
What is the purpose of useMemo?
What is the purpose of useCallback?
What is the difference between useMemo and useCallback?
Explain the syntax of useMemo.
Explain the syntax of useCallback.
When should you use useMemo?
When should you use useCallback?
What is useContext?
How do you create a Context?
How do you provide values through Context?
How do you consume values from Context?
How do you fetch values from Context?
What is the purpose of createContext()?
What is the difference between local state and global state?
How can you make a state globally accessible?
useReducer
What is useReducer?
When would you use useReducer instead of useState?
Explain the concept of dispatch.
How does dispatch work internally?
What scenarios are suitable for useReducer?
Can useContext and useReducer be used together?
How do you access dispatch across the application?
useRef
What is useRef?
What are the use cases of useRef?
Difference between useRef and useState.
How do you access DOM elements using useRef?
Custom Hooks
What is a custom hook?
Difference between a normal JavaScript function and a React Hook.
Why do custom hooks start with use?
Can a custom hook return multiple values?
Why would you create a custom hook?

Higher Order Components
What is a Higher Order Component (HOC)?
How does an HOC work?
What problems do HOCs solve?
Difference between HOC and Hooks.
Real-world examples of HOCs.
React Performance & Production Debugging

Dashboard Performance
---------------------
Suppose only the Dashboard page is slow. How would you debug it?
What are possible reasons for dashboard slowness?
How would you identify unnecessary re-renders?
How would you optimize a dashboard with many charts and widgets?
How would you handle large datasets in React?
What is virtualization?

Production Issues
-----------------
A user reports that the application becomes slow after navigating multiple pages. How would you investigate?
How do you debug frontend issues in production?
If you cannot access the user's browser Network tab, how will you diagnose the issue?
How would you ensure this problem doesn't happen again?
How do you proactively monitor frontend performance?
What performance optimizations would you implement in React applications?

Node.js Questions
-----------------
Concurrency & Async
Difference between synchronous and asynchronous operations.
When would you execute tasks in parallel?
When would you execute tasks sequentially?
Explain Promise.all().
Explain Promise.allSettled().
What is concurrency in Node.js?
Difference between concurrency and parallelism.
How does Node.js achieve concurrency?
What is the Event Loop?
libuv
What is libuv?
What operations are handled by libuv's thread pool?
How many threads does the libuv thread pool have by default?
Can the thread pool size be increased?
Event Loop
What are macrotasks?
What are microtasks?
Difference between microtasks and macrotasks.
Which has higher priority: microtasks or macrotasks?
How do you create microtasks?
How do you create macrotasks?
Explain setTimeout().
Explain setInterval().
Difference between setTimeout() and setInterval().
What is setImmediate()?
What is process.nextTick()?

Express.js Questions
--------------------
Have you worked with Express.js?
Explain Express middleware.
What is the purpose of middleware?
What are the parameters of a middleware function?
What is the purpose of next()?
Explain request flow through middleware.
What is authentication middleware?
What is error-handling middleware?
How would you structure an Express application?

Authentication & Security
-------------------------
JWT
What is stateless authentication?
How does JWT authentication work?
How is a JWT generated?
How is a JWT verified?
Can JWT tokens expire?
How do refresh tokens work?

What information should be stored in a JWT?
Session Authentication
----------------------
What is session-based authentication?
Difference between session-based and JWT authentication.
Where is session data stored?
How does session management work in Express?
OAuth
Difference between JWT and OAuth.
What problem does OAuth solve?
How does OAuth login work?
Authorization
What is Role-Based Access Control (RBAC)?
Difference between authentication and authorization.
How would you implement role-based authorization?
How would you restrict API access based on roles?
Password Security
What is hashing?
Why do we hash passwords?

Difference between hashing and encryption.
Difference between hashing and JWT.
Why use bcrypt instead of SHA256?
What is salting?

Common Security Risks
---------------------
What security implementations have you used in your projects?
What is XSS?
How do you prevent XSS?
What is CSRF?
How do you prevent CSRF?
What is SQL Injection?
How do you prevent SQL Injection?
What is Broken Access Control?
What is Sensitive Data Exposure?

What is Rate Limiting?
How do you secure APIs?

GraphQL Questions
----------------
What is GraphQL?
How does GraphQL communicate with frontend and backend?
What are GraphQL Queries?
What are GraphQL Mutations?
What are Resolvers?
Difference between REST and GraphQL.
How does GraphQL reduce over-fetching?
How does GraphQL reduce under-fetching?
Does GraphQL always improve performance?
Can GraphQL be slower than REST?
What is the N+1 Query Problem?

AWS Questions
-------------
What AWS services have you worked with?

What is AWS Lambda?
What is serverless computing?
How does Lambda work?
What can trigger a Lambda function?
Have you created scheduled Lambda jobs?
How does EventBridge trigger Lambda?
Difference between cron and rate expressions.
Can Lambda access S3 bucket objects?
How does Lambda read objects from S3?
What IAM permissions are required?
How can S3 trigger Lambda?

Full Stack / Architecture Questions
------------------------------------
How does frontend communicate with backend?
REST vs GraphQL.
How do React applications communicate with Express APIs?
How do you authenticate API requests?
How would you design a scalable dashboard?
How would you optimize API performance?
How would you handle production performance issues?
How would you architect a secure full-stack application?
