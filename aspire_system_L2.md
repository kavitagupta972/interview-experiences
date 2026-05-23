# React.js Interview Questions

## React Fundamentals

* What is React and what problem does it solve?
* What is Virtual DOM?
* Difference between Virtual DOM and Real DOM.
* What is JSX?
* What is the difference between functional and class components?
* What are props and state in React?
* What is one-way data binding?
* What is lifting state up?
* What are controlled and uncontrolled components?
* What are synthetic events in React?
* Explain React lifecycle methods.
* What is React Fiber Architecture?
* What is React Reconciliation?
* What are React Fragments and why are they used?
* What are Higher Order Components (HOC)?
* What are Pure Components?
* What is React.memo?
* What is the difference between React.memo and useMemo?
* What is the difference between useMemo and useCallback?
* What are custom hooks?
* What are React Hooks and why were they introduced?
* Explain useState, useEffect, useRef, useContext, useReducer.
* Explain useLayoutEffect.
* What are rules of hooks?
* How does React handle re-rendering?
* How do keys work in React lists?
* What is lazy loading in React?
* What is code splitting?
* What is concurrent rendering in React?
* What is Server Side Rendering (SSR)?
* Difference between CSR and SSR.
* What is hydration in React?
* What are Error Boundaries?
* What is React Strict Mode?
* Explain React Portals.
* What is the current React version you worked with?

---

## React Routing

* What is React Router?
* Difference between BrowserRouter and HashRouter.
* What are Protected Routes?
* How do you implement role-based routing?
* Difference between nested routes and dynamic routes.
* How do you handle route guards in React?

---

## Redux

* What is Redux?
* Why do we need Redux?
* Explain Redux Architecture.
* What is immutability in Redux?
* What is Redux middleware?
* Difference between Redux Thunk and Redux Saga.
* What is yield in Redux Saga?
* Explain action creators and reducers.
* What is Redux Toolkit?
* Difference between Context API and Redux.
* How does Redux prevent unnecessary re-renders?

---

## React Performance Optimization

* How do you optimize React applications?
* What causes unnecessary re-renders?
* How do you optimize large lists?
* Explain memoization in React.
* Difference between debounce and throttle.
* What is bundle optimization?
* How does tree shaking work?
* Explain lazy loading and suspense.
* How do you analyze bundle size?

---

## React Build & Tooling

* What is webpack?
* Difference between webpack and Vite.
* What is Rollup?
* What are bundlers?
* Explain Babel.
* What is transpilation?
* What is package.json?
* Difference between package.json and package-lock.json.
* What is a PWA?
* What is Atomic Design Pattern?
* Explain environment variables in React.
* How do you configure multiple environments?

---

## API Handling in React

* What is Axios?
* Difference between Axios and Fetch.
* What are Axios interceptors?
* What is CORS?
* How do you handle API failures gracefully?
* How do you implement retry logic for APIs?
* How do you cancel API requests?

---

## UI/UX & Frontend Architecture

* Difference between px, rem, em, and pt.
* What is responsive design?
* How do you support different UI for different clients?
* How would you change form position dynamically without deployment/code changes?
* How do you implement feature flags in frontend?
* Explain pluralization and interpolation in i18n.

---

## React Coding Questions

* Create a reusable card component and render employee list from API.
* Implement Protected Route.
* Create a custom hook.
* Create two components where typing in one updates another instantly.
* Filter API response based on user input.
* Find the most repeated number in an array.
* Find popular value from array.
* Implement debounce search.
* Create infinite scroll component.
* Build dynamic form rendering.
* Create reusable modal component using hooks.

---

# Node.js Interview Questions

## Node.js Fundamentals

* Is Node.js single-threaded or multi-threaded?
* Explain the Node.js Event Loop and its phases.
* What is non-blocking I/O?
* What are worker threads?
* What is clustering in Node.js?
* How does Node handle concurrency?
* What are streams in Node.js?
* Difference between process.nextTick() and setImmediate().
* What is middleware in Express.js?
* Explain Express.js request lifecycle.
* How do you structure a Node.js application?
* What are common Node.js performance bottlenecks?
* How do you optimize Node.js memory usage?
* How do you handle centralized error handling?
* How do you build/compile Node.js applications?

---

## Express.js

* What is Express.js?
* Explain express.Router().
* Why should error middleware be defined last?
* How do you separate admin and public routes?
* How do you implement authentication in Express?
* What is stateless architecture?
* Why should sessions not be stored in local variables?
* How do you implement JWT authentication?
* Where should JWT be stored (Cookie vs LocalStorage)?
* How do you prevent NoSQL injection?
* How do you sanitize request body?

---

## Backend Architecture & System Design

* Explain Monolithic vs Microservices architecture.
* Difference between Monorepo and Multi-repo.
* How do you deploy microservices?
* How do you handle production failures?
* How do you design scalable APIs?
* How do you handle 1000+ concurrent users?
* What monitoring tools have you used?
* How do you log and track production errors?
* Explain API Gateway architecture.
* What is service discovery?
* How do you handle distributed transactions?
* Explain idempotency in APIs.

---

## Database & Performance

* How do you optimize slow MySQL queries?
* What is indexing?
* Explain SQL query optimization.
* What tools do you use to analyze slow queries?
* Difference between SQL and NoSQL.
* What is MongoDB aggregation?
* Difference between $match and $filter.
* What are atomic operations in MongoDB?
* How do you avoid race conditions?
* Explain TTL indexes.
* How do you handle database connection pooling?

---

## Queue Systems & Async Processing

* What is Amazon SQS?
* Why are queues important?
* How do you avoid duplicate processing?
* How do you test email queue systems?
* How do you process long-running jobs?
* Difference between SQS, Kafka, and RabbitMQ.
* How do you ensure queue reliability?

---

## Security

* How do you secure APIs?
* How do you protect credentials?
* How do you prevent SQL Injection and XSS?
* What is CORS?
* How do you implement rate limiting?
* How do you secure sensitive environment variables?
* Explain OWASP Top 10 basics.

---

## Node.js Coding Questions

* Build REST API with Express.
* Implement middleware for authentication.
* Build rate limiter middleware.
* Create file upload API.
* Implement pagination API.
* Build retry mechanism for failed APIs.
* Create caching layer using Redis.
* Build scalable notification service.

---

# AWS Interview Questions

## AWS Fundamentals

* Which AWS services have you used?
* What is AWS IAM?
* Difference between IAM User and IAM Role.
* What are AWS Security Groups?
* Explain VPC architecture.
* Difference between Default VPC and Custom VPC.
* What is Route53?
* What is CloudFront?
* What is API Gateway?
* What is AWS Lambda?
* When should Lambda be preferred over EC2?
* What are Lambda Layers?
* What causes Lambda cold starts?
* Difference between Reserved Concurrency and Provisioned Concurrency.
* How do you deploy applications on AWS?

---

## Serverless Architecture

* What is serverless computing?
* How do Lambda triggers work?
* How do you secure serverless applications?
* How do you handle retries in Lambda?
* How do you process large files with Step Functions?
* What is Lambda@Edge?
* When should you use Lambda@Edge?

---

## Storage & Database

* What is Amazon S3?
* Explain S3 event triggers.
* How do you prevent duplicate processing from S3 triggers?
* Difference between RDS and DynamoDB.
* What is Amazon RDS?
* How do you optimize RDS performance?

---

## Networking & Scaling

* What is Auto Scaling?
* What is Load Balancer?
* Difference between ALB and NLB.
* How does Route53 latency-based routing work?
* How do you handle bot traffic?
* Explain throttling in API Gateway.
* Difference between Stage-level throttling and API-key throttling.

---

## AWS Security

* How do you secure AWS credentials?
* Where should secrets be stored?
* Explain AWS Secrets Manager.
* What is KMS?
* Best practices for API security in AWS.
* How do Security Groups differ from NACLs?

---

## DevOps & Deployment

* How do you deploy to production and staging?
* What is CI/CD?
* Which CI/CD tools have you used?
* Explain blue-green deployment.
* What is rolling deployment?
* How do you monitor AWS infrastructure?
* Which monitoring tools have you used?
* Explain CloudWatch logs and metrics.

---

## AWS Architecture Scenario Questions

* Design a digital asset purchase system using AWS services.
* How do you handle failed background jobs?
* How do you notify users about pending processing?
* How do you build highly available APIs?
* How do you architect systems for high traffic globally?

---

# Team Management & Agile Interview Questions

## Leadership

* How do you manage a development team?
* How do you mentor junior developers?
* How do you review team members’ code?
* What do you check during code reviews?
* How do you maintain coding standards?
* How do you ensure knowledge sharing in the team?
* How do you handle underperforming team members?
* How do you handle conflicts in the team?
* How do you motivate the team during deadlines?
* How do you distribute tasks across team members?

---

## Agile & Scrum

* What is Agile methodology?
* What is Scrum?
* What is a Sprint?
* How long is a typical Sprint?
* What are Sprint Planning meetings?
* What is Daily Standup?
* What is Sprint Retrospective?
* What is Sprint Review?
* What are Story Points?
* How do you estimate Story Points?
* Maximum story points taken in a sprint?
* What happens if stories are not completed in a sprint?
* How do you handle changing requirements during a sprint?
* What tools do you use for Agile tracking?

---

## Collaboration & Delivery

* How do you communicate with stakeholders?
* How do you manage client expectations?
* How do you handle production incidents?
* How do you prioritize bugs vs feature work?
* How do you ensure timely delivery?
* How do you coordinate across frontend/backend/devops teams?
* What is your approach toward technical debt?

---

# Mobile Development Questions

## React Native vs Flutter

* Difference between React Native and Flutter.
* How do you decide which framework to use?
* Advantages and disadvantages of both.
* Performance comparison.
* Community and ecosystem comparison.
* Deployment process for App Store and Play Store.
* How do OTA updates work?

---

# AI & Productivity Questions

* Which AI tools are you currently using?
* How does AI improve developer productivity?
* How do you validate AI-generated code?
* What are risks of using AI-generated code?
* How do you integrate AI into development workflow?

* # Compiled Interview Questions

## Event-Driven Architecture & Distributed Systems

1. Look at the technical nuances of how it was implemented. What was your role inside it?

2. Talk about some complex scenarios you implemented in event-driven architecture.

3. What technology stack and architectural approach did you use for implementing event-driven architecture?

4. How did your team handle failures in asynchronous workflows?

5. How do you handle acknowledgement failures in event-driven architecture?

6. If a message is picked up but not acknowledged back to the queue, how do you handle that situation?

7. How do retries, visibility timeout, and DLQ work in event-driven systems?

8. How do you prevent duplicate processing in event-driven architecture?

9. How do you ensure eventual consistency across distributed services?

10. How did you implement decentralized monitoring in distributed systems?

11. Why did you choose Lambda for transaction-heavy systems?

12. Why not use API Gateway policies instead of separate Lambda functions?

13. What kind of dynamic business logic required a separate Lambda for cars?

14. If car validations are static, why introduce Lambda at all?

---

# Backend / Node.js / REST API

15. How do you optimize Node.js or Express APIs?

16. How do you improve REST API performance?

17. What performance optimization problems did you solve in your project?

18. How do you optimize task evaluation in REST APIs?

19. How do you handle long-running queries in PostgreSQL with Lambda limitations?

20. How do you move heavy processing out of request-response lifecycle?

21. How do you handle background processing in backend systems?

22. What are the common causes of slow REST APIs?

23. How do you optimize database-heavy APIs?

24. How do you reduce event-loop blocking in Node.js?

25. How do you use Promise.all for API optimization?

26. How do caching strategies improve backend performance?

---

# Authentication & Security

27. Can you elaborate on authentication implementation?

28. How did you implement JWT authentication?

29. How does token-based authentication work?

30. How do you handle authorization and RBAC?

31. How do refresh tokens work?

32. Why use JWT over session-based authentication?

---

# React / Frontend Architecture

33. How would you implement a stock trading application with real-time updates?

34. How would you render 500+ stock tiles efficiently?

35. How would you maintain UI performance under heavy real-time updates?

36. What frontend architecture would you choose for asynchronous modules?

37. How would you achieve rendering within 10ms for large dynamic UIs?

38. What technology choices would you make for a highly dynamic dashboard?

39. What optimizations would you implement in React for real-time systems?

---

# React 18 / React Fiber

40. What features of React 18 did you use in your project?

41. Why did you migrate to React 18?

42. What is automatic batching in React 18?

43. What is concurrent rendering?

44. What is useTransition and where did you use it?

45. What is React Fiber?

46. How does React Fiber improve rendering performance?

47. What problem did React Fiber solve?

48. What is reconciliation in React?

49. What are render phase and commit phase in React Fiber?

50. How does React prioritize updates internally?

---

# Axios / API Communication

51. What are Axios interceptors?

52. What is the difference between request and response interceptors?

53. How did you use Axios interceptors in your project?

54. How do you handle token refresh using interceptors?

55. How do you centralize API error handling?

---

# SDK Optimization & Performance Engineering

56. Explain a complex scenario where you improved SDK performance.

57. What bottlenecks did you identify in the SDK?

58. How did you optimize websocket usage?

59. How did you reduce unnecessary re-renders?

60. How did you modularize the SDK?

61. How did you fix memory leaks in frontend systems?

62. How did you optimize bundle size?

63. How did you optimize high-frequency UI updates?

64. How did you improve frontend runtime performance?

---

# AI Tools / GitHub Copilot / Productivity

65. How do you measure productivity improvement using AI tools like GitHub Copilot?

66. What metrics did you use to measure productivity enhancement?

67. What inputs did you provide to Copilot for unit test generation?

68. Does Copilot use only code context or also user stories?

69. How do you validate AI-generated unit tests against business requirements?

70. If the implementation is addition but user story expects multiplication, how do you justify Copilot-generated tests?

71. What are the limitations of AI-generated code/tests?

72. How do you ensure engineering quality with AI-assisted development?

---

# React Coding / Autocomplete / Debouncing

73. Implement an autocomplete/search suggestion component in React.

74. How would you fetch and filter product data dynamically while typing?

75. Should you fetch data on button click or during typing?

76. How would you implement autocomplete using DummyJSON products API?

77. How would you use useEffect to fetch products initially?

78. How would you filter products locally using useState?

79. Why is local filtering suitable for 500–1000 records?

80. When should filtering move to backend instead of frontend?

81. What is debouncing?

82. Why is debouncing important in autocomplete systems?

83. How do you implement debounce in React?

84. What is the difference between debounce and throttle?

85. How do you avoid unnecessary API calls during typing?

86. How do you cancel previous API requests in autocomplete systems?

87. How do you optimize rendering in large search result lists?

---

# General Architecture / System Design

88. How do you balance scalability versus overengineering?

89. How do you decide whether logic belongs in API Gateway, Lambda, or backend services?

90. How do you separate infrastructural concerns from business logic?

91. How do you design resilient distributed systems?

92. How do you improve observability in microservice architectures?

93. How do you manage correlation IDs across services?

94. How do you handle partial failures in distributed systems?

95. What architectural tradeoffs do you consider while choosing serverless vs persistent services?


