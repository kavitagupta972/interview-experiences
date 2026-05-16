# Aspire System – Interview Preparation Notes

**Date:** 16 May 2026

---

# React Questions

## React Architecture & Concepts

1. Prop drilling in React applications
2. Why use React over other libraries or frameworks?
3. React Fiber architecture
4. React as a Single Page Application (SPA)
5. How routing is handled internally in React
6. Protected Routes in React – how to protect routes
7. Authentication and Authorization in SPA applications
8. State management in large React applications
9. Flow of Redux
10. Login API flow → Redux Store → Protected Routes → Authorized Screens

## React Components & Forms

1. Controlled vs Uncontrolled Components
2. When to use controlled components
3. Most common use cases of controlled components in forms
4. Key attribute in React lists
5. Other ways to write UI in React apart from JSX

## React Performance & Optimization

1. useMemo vs useCallback
2. Performance optimization in React applications
3. Avoiding unnecessary re-renders

## React Reusability Patterns

1. Custom Hooks vs HOC (Higher Order Components)
2. Real-time use cases of custom hooks
3. Sharing stateful logic using custom hooks
4. HOCs returning enhanced components with additional behavior

---

# JavaScript Questions

## Core JavaScript Concepts

1. Closures in JavaScript
2. Real-time use cases of closures
3. ES6 features
4. Difference between Rest and Spread operators
5. Concept of Event Loop in JavaScript
6. Difference between async/await and Promises
7. When to use async/await vs Promises
8. Difference between var, let, and const
9. Debouncing and Throttling

## Asynchronous JavaScript

1. How to call multiple async APIs in parallel
2. How to call dependent async APIs
3. Promise.all vs Promise.allSettled
4. Handling async operations in JavaScript

---

# Node.js Questions

## Node.js Fundamentals

1. Node.js is single-threaded – then how does it scale?
2. Event Loop in Node.js
3. Middleware in Express.js
4. Different types of middleware in Express
5. Centralized error handling in Node.js
6. Structure of a Node.js application

## API & Backend Design

1. How to optimize API performance in Node.js
2. API versioning
3. Request flow in Node.js applications:

```text
Client Request
   ↓
Route
   ↓
Middleware
   ↓
Controller
   ↓
Service
   ↓
Database
   ↓
Response
```

## Authentication & Authorization

1. How authentication works in Node.js applications
2. Authorization in Node.js
3. Authentication middleware
4. Different ways to implement authorization
5. Security best practices in Node.js applications

---

# MongoDB Questions

## MongoDB Basics

1. Difference between SQL and MongoDB
2. Embedding vs Referencing in MongoDB
3. Indexing in MongoDB

## Aggregation Framework

1. Aggregation Pipeline in MongoDB
2. Match and Group stages in Aggregation
3. Optimizing aggregation queries

---

# AWS Questions

## AWS Services

1. Difference between EC2 and Lambda
2. When to use AWS Lambda
3. How to store/upload data in S3
4. AWS services overview

---

# Frequently Asked Interview Discussion Topics

## React + Redux

1. Flow of Redux
2. Protected routes and authorization flow
3. State management in large applications

## JavaScript Optimization

1. Debouncing vs Throttling
2. Closures and practical examples
3. Async operations handling

## Backend & Database

1. API performance optimization
2. Aggregation pipeline optimization
3. MongoDB indexing strategies
4. Authentication and authorization flow

---

# Programming / Machine Coding Question

## Employee Management Application (React)

### Problem Statement

Build an employee management application that efficiently fetches and displays employee data while solving performance and data management issues.

The current application has the following problems:

* Direct API calls inside components
* Redundant API calls for the same employee details
* Poor state management
* No caching mechanism
* No proper error handling
* No pagination support
* Unnecessary re-renders

### Requirements

#### 1. Create a Custom Hook – `useFetch`

Build a reusable custom hook called `useFetch` that:

* Accepts a URL parameter
* Handles all API-fetching logic
* Returns:

  * fetched data
  * loading state
  * error state/message

#### 2. Implement Caching Logic

Add caching inside the `useFetch` hook:

* Cache should be URL-specific
* If the same employee details are requested again:

  * Return cached data
  * Avoid redundant API calls
* Improve application performance

#### 3. Employee List Component

Build an employee list component that:

* Fetches employee data
* Displays employees in paginated form
* Shows limited employees per page
* Includes pagination controls
* Allows navigation between pages

#### 4. Employee Details Component

When the user clicks on an employee name:

* Fetch detailed employee information
* Use the `useFetch` custom hook
* Display employee details in a separate section
* Handle loading and error states properly

#### 5. Proper Error Handling

Implement robust error handling throughout the application:

* Display meaningful error messages
* Prevent blank screens or crashes
* Handle failed API requests gracefully

#### 6. Performance Optimization

Optimize the application using React best practices:

* Prevent unnecessary re-renders
* Use memoization where appropriate
* Use React hooks efficiently
* Maintain clean and scalable architecture

#### 7. Expected Deliverables

* Complete working React application
* Clean folder structure
* Reusable custom hooks
* Pagination support
* Optimized rendering
* Proper loading and error states
* Maintainable and scalable codebase

---

# Quick Revision Topics

## React

* React Fiber
* Protected Routes
* Redux Flow
* Controlled vs Uncontrolled Components
* useMemo vs useCallback
* Custom Hooks vs HOC

## JavaScript

* Closures
* Event Loop
* Promises
* Async/Await
* Debouncing & Throttling
* var vs let vs const

## Node.js

* Middleware
* Centralized Error Handling
* API Optimization
* Authentication & Authorization
* API Versioning

## MongoDB

* Aggregation Pipeline
* Indexing
* Embedding vs Referencing

## AWS

* EC2 vs Lambda
* S3 Storage
* Lambda Use Cases
