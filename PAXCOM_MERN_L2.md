Based on the conversation you've shared, this L2 round was primarily evaluating **System Design, Distributed Systems, Payment Systems, Scalability, Reliability, Production Support, and Leadership**. Here's a compiled list of the questions, organized by topic.

# 1. Project Architecture & Experience

### Q1. You mentioned handling 500,000 daily transactions. Explain:

* Overall system architecture
* Your role in the system
* How data flowed through the system
* How scalability was achieved
* What databases were used
* What challenges you faced

### Q2. Explain the microservices architecture used in your project.

* Why microservices?
* Service boundaries
* Communication between services
* Advantages over monolithic architecture

### Q3. Were the APIs provided to you or did you develop them?

* API ownership
* Frontend-backend collaboration
* API design involvement
* Node.js experience

### Q4. How do frontend applications communicate with microservices?

* API Gateway
* Authentication
* API aggregation
* Caching strategies

---

# 2. Payment System Design

### Q5. Design a scalable payment processing system for Amazon/Flipkart.

Cover:

* Order placement
* Payment processing
* Inventory management
* Refunds
* Notifications
* Retry mechanisms
* High traffic sale events

Expected discussion:

* High-level architecture
* Service decomposition
* Database strategy
* Event-driven architecture
* Scalability

---

# 3. Inventory and Order Management

### Q6. How would you handle inventory reservation?

Discuss:

* Inventory locking
* Temporary reservation
* Reservation timeout
* Stock deduction

### Q7. Inventory reserved but payment failed. How will you rollback?

Topics:

* Saga Pattern
* Compensating Transactions
* Kafka events
* Inventory release

### Q8. UPI payment fails and user retries with Net Banking.

Questions:

* Should inventory be released immediately?
* How will payment retries work?
* How many payment attempts are allowed?
* How will order state be maintained?

### Q9. Difference between:

* Reserved Inventory
* Available Inventory
* Confirmed Inventory

---

# 4. Idempotency & Duplicate Payment Prevention

### Q10. What happens if a user clicks the Pay button three times?

Discuss:

* Duplicate payment prevention
* Race conditions
* Payment consistency

### Q11. What is an Idempotency Key?

Explain:

* Why it is needed
* Where it is generated
* Storage mechanism

### Q12. How would you implement idempotency in Node.js?

Expected:

* Redis
* Database
* Middleware design

### Q13. What if three requests reach the backend simultaneously?

Discuss:

* Concurrency control
* Race conditions
* Locking mechanisms

### Q14. How would Redis SETNX help?

Topics:

* Atomic operations
* Distributed locking

---

# 5. Distributed Transactions

### Q15. Why can't we use database transactions across microservices?

Expected:

* Separate databases
* Distributed system challenges

### Q16. What is the Saga Pattern?

Explain:

* Choreography
* Orchestration
* Compensating transactions

### Q17. When would you choose Saga over 2PC (Two-Phase Commit)?

---

# 6. Eventual Consistency

### Q18. Explain eventual consistency in payment systems.

Expected:

* Temporary inconsistency
* Final consistency
* Real examples

### Q19. Why is eventual consistency acceptable?

### Q20. Where should strong consistency be maintained?

Examples:

* Payment records
* Inventory count
* Order confirmation

### Q21. Explain CAP Theorem.

Topics:

* Consistency
* Availability
* Partition tolerance

### Q22. How does eventual consistency help scalability?

---

# 7. Kafka & Asynchronous Communication

### Q23. Which services should be synchronous and which asynchronous?

Expected:

Synchronous:

* Order
* Inventory
* Payment

Asynchronous:

* Notifications
* Analytics
* Reports

### Q24. Why use Kafka?

Discuss:

* Scalability
* Decoupling
* Replay capability

### Q25. How do Kafka consumers work?

### Q26. What is Kafka consumer lag?

### Q27. What happens when a consumer goes down?

### Q28. What is a Dead Letter Queue (DLQ)?

### Q29. How would you retry failed Kafka events?

---

# 8. Payment Failure Scenarios

### Q30. Payment succeeds at gateway but service crashes before updating order status.

Discuss:

* Webhooks
* Reconciliation jobs
* Event recovery

### Q31. How would you reconcile payment mismatches?

### Q32. What is payment reconciliation?

### Q33. How frequently should reconciliation run?

### Q34. How do payment gateways notify success?

Expected:

* Webhooks
* Polling

### Q35. What if webhook fails?

---

# 9. Scalability Questions

### Q36. How would you scale a payment system during a flash sale?

Expected:

* Auto-scaling
* Load balancing
* Queue management

### Q37. How would you handle 10x traffic?

### Q38. What happens when traffic exceeds system capacity?

### Q39. Explain backpressure handling.

### Q40. How would you prevent overselling inventory?

---

# 10. Database Design

### Q41. Which database would you use for:

* Orders
* Payments
* Inventory
* Analytics

### Q42. SQL vs NoSQL?

### Q43. What is database sharding?

### Q44. How would you shard transaction data?

### Q45. What are read replicas?

### Q46. How would caching help?

Expected:

* Redis
* Session management
* Inventory lookups

---

# 11. Production Support & Leadership

### Q47. Tell me about a major production issue you faced.

Expected:

* Incident description
* Investigation
* Resolution

### Q48. How do you handle client pressure during production outages?

### Q49. What is your approach during a P1 incident?

Expected:

* War room creation
* Communication plan
* Escalation strategy

### Q50. What metrics would you monitor in production?

Examples:

* Error rates
* API latency
* Kafka lag
* Success rates

### Q51. How would you perform Root Cause Analysis (RCA)?

### Q52. How do you communicate with stakeholders during outages?

---

# 12. Leadership & Ownership

### Q53. As a Senior Engineer, how do you lead incident resolution?

### Q54. How do you coordinate:

* Frontend team
* Backend team
* DevOps team

during a critical outage?

### Q55. How do you mentor junior developers during production incidents?

### Q56. What decisions would you take if:

* Client is escalating
* Revenue is impacted
* System is partially down

---

# 13. Advanced Follow-Up Questions

### Q57. How would you design a refund system?

### Q58. How would partial refunds work?

### Q59. How would you implement rate limiting?

### Q60. How would you implement circuit breakers?

### Q61. What is the Outbox Pattern?

### Q62. How do you guarantee exactly-once processing?

### Q63. At-least-once vs At-most-once vs Exactly-once delivery?

### Q64. How would you detect duplicate payment events?

### Q65. How would you audit financial transactions?
