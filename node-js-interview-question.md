# 1. Node.js Fundamentals & Internals

1. What is **Node.js**, and how is it different from traditional server-side runtimes?
2. What is the **Event Loop** in Node.js?
3. If Node.js is **single-threaded**, how does it handle **multiple requests concurrently**?
4. What is the **V8 Engine**, and why is it used in Node.js?
5. What is **libuv**, and what role does it play in Node.js?
6. How does Node.js **handle asynchronous operations** internally?
7. How do **Promises, async/await, setTimeout, and setImmediate** execute in Node.js?
8. What is the **execution order between microtasks and macrotasks** in Node.js?

---

# 2. Concurrency & Multithreading

9. What is the difference between **Cluster and Worker Threads** in Node.js?
10. When should you use **Cluster**?
11. When should you use **Worker Threads**?
12. How does Node.js handle **CPU-intensive tasks**?

---

# 3. Streams, Buffers & I/O

13. What is the difference between **blocking and non-blocking I/O**?
14. What is a **Buffer** in Node.js?
15. What are **Streams**, and what types of streams exist in Node.js?
16. How do **Streams and Buffers work together**?
17. What is **Backpressure**, and how do you handle it?
18. What are **best practices when reading large files or streaming data**?

---

# 4. Memory Management

19. What is a **Memory Leak** in Node.js?
20. How does **Garbage Collection** work in Node.js?
21. How do you **detect and debug memory leaks**?

---

# 5. Messaging Queue & Background Processing

22. What is a **Message Queue**?
23. Why do we use **Message Queues** in backend architectures?
24. What **message queue technologies** have you used?
25. What are **background workers**, and how do they work?
26. What is a **Dead Letter Queue (DLQ)**?
27. How does the **producer–consumer pattern** work?
28. How do you **retry failed messages**?
29. How do you **handle duplicate messages**?
30. How do you **maintain message ordering**?
31. What is the difference between **message queue and pub/sub architecture**?

---

# 6. Authentication & Authorization

32. What is the difference between **Authentication and Authorization**?
33. What is a **stateful system** vs **stateless system**?
34. How does **session-based authentication** work?
35. How does **JWT authentication** work?
36. What is the **structure of a JWT token**?
37. How does the **JWT signature verify authenticity**?
38. What algorithms are used to **sign JWT tokens**?
39. How do you **secure the JWT secret key**?
40. How does JWT **store payload data**?

---

# 7. Caching

41. What is **caching**, and why is it important?
42. What types of **caching strategies** have you used?
43. How do you **invalidate or revalidate cached data**?
44. What is the difference between **in-memory cache and distributed cache**?

---

# 8. Scalability & Infrastructure

45. What is **Vertical Scaling**?
46. What is **Horizontal Scaling**?
47. When should you use **Vertical Scaling vs Horizontal Scaling**?
48. How do you implement **horizontal scaling in Node.js applications**?

---

# 9. Proxy, Load Balancer & API Gateway

49. What is a **Forward Proxy**?
50. What is a **Reverse Proxy**?
51. What is a **Load Balancer**?
52. How does a **Load Balancer distribute traffic**?
53. What is an **API Gateway**?
54. When should you use an **API Gateway**?
55. How would you **implement an API Gateway in a Node.js system**?

---

# 10. Rate Limiting & Traffic Control

56. What is **Rate Limiting**?
57. What is **Fixed Window Rate Limiting**?
58. What is **Sliding Window Rate Limiting**?
59. What is the **Leaky Bucket Algorithm**?
60. What is the **Token Bucket Algorithm**?

---

# 11. Databases & Data Modeling

61. What is **database indexing**?
62. How do you **create and use indexes effectively**?
63. What is the difference between **SQL and NoSQL databases**?
64. When should you choose **SQL vs NoSQL**?
65. What is **embedding vs referencing** in NoSQL databases?
66. How do you **perform joins in NoSQL databases**?

---

# 12. Pagination & Query Optimization

67. What is **pagination in APIs**?
68. What is the difference between **offset-based pagination and cursor-based pagination**?
69. What are common **query optimization techniques**?
70. How do you avoid **N+1 query problems**?

---

# 13. MongoDB Concepts

71. What is an **Aggregation Pipeline** in MongoDB?
72. How does the **Aggregation Pipeline work**?
73. How does **MongoDB maintain atomicity**?
74. Is MongoDB **atomic at document level, collection level, or database level**?
75. What happens if **insertMany fails in the middle of execution**?

---

# 14. Distributed Databases

76. What is **Sharding**?
77. What is **Partitioning**?
78. What is **Replication**?
79. What is **Fault Tolerance**, and how can it be achieved?

---

# 15. API Performance & Troubleshooting

80. If an **API is slow**, how do you troubleshoot it?
81. If **CPU usage becomes high and the event loop gets blocked**, what will you do?
82. If there is a **sudden spike in traffic**, how do you handle it?

---

# 16. Logging, Monitoring & Observability

83. How do you **handle errors in an Express.js application**?
84. How do you **maintain logs in a backend application**?
85. In a **monorepo with multiple services**, how do you identify where an error occurred?
86. How do you **improve logging in distributed systems**?
87. What **external logging/monitoring tools** have you used?

---

# 17. Web Security

88. What is **CORS**, and how does it work?
89. How do you **handle CORS in backend applications**?
90. What is **CSRF**, and how do you protect against it?

---

# 18. API Versioning & Compatibility

91. How do you **handle API versioning without breaking existing clients**?

---

# 19. System Resilience & Failure Handling

92. If a **downstream service fails**, how do you prevent your API from failing?
93. What is the **Circuit Breaker pattern**?
94. If a **third-party API is slow**, how do you handle it?
95. How do you **handle production errors in backend systems**?

---

# 20. Distributed Systems Concepts

96. What is the **CAP Theorem**?
97. What are **ACID properties** in databases?

---

# 21. Microservices Architecture

98. What are **Microservices**, and how are they different from Monoliths?
99. How do **microservices communicate** with each other?
100.  Why should **each microservice have its own database**?
101.  What is **service isolation**?
102.  What is the **Saga Pattern**?
103.  How do you handle **failures between synchronous services (A → B → C)**?
104.  What are **synchronous vs asynchronous communication in microservices**?
105.  How do you implement **service discovery**?
106.  How do you handle **distributed transactions**?

---

# 22. Session Management

107. If you run **multiple Node.js instances**, how do you **manage sessions**?

---

# 23. Software Design Principles

108. What are the **SOLID principles** in software design?

---

# 24. System Design / Coding

109. Design a **Credit Card class** that supports:

- Credit transactions
- Debit transactions
- Balance handling
- Transaction history

---

# 25. Data Migration & Reliability

110. How do you **copy data from one database to another at the application level**?
111. What is the **safest way to perform such migrations without data loss**?

---

# 26. Backend Performance Optimization

**How can you improve the performance of a backend application?**

Key approaches:

- Keep the **event loop non-blocking**
- **Optimize database access**
  - Reduce number of queries
  - Proper indexing
  - Use projections
  - Efficient aggregation
  - Avoid N+1 queries
- Use **pagination**
- Implement **caching**
- Enable **compression**
- Use **clustering / horizontal scaling**
- Apply **circuit breaker pattern**

---

# 27. Backend Security

**How can you improve the security of a backend application?**

### Secure communication

- HTTPS
- API Gateway

### Authentication

- OAuth
- MFA
- Strong password policies
- Encryption

### Authorization

- Scope-based access control

### API protection

- Rate limiting
- API versioning

### Input validation

- Schema validation
- ORM/ODM protection against injection

### Browser security

- CORS
- CSRF
- XSS protection
- CSP headers

### Secure error handling

- Avoid exposing internal system details

---
