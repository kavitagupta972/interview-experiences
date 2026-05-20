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

